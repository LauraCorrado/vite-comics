<script>
import { shopItems } from "../../data/menuLists"
export default {
    data() {
        return {
            shopItems
        }
    }
}
</script>
<template>
    <div class="py-5">
        <div class="d-flex align-items-center justify-content-around">
            <div v-for="item, index in shopItems" :key="`shop-${index}`" class="d-flex align-items-center">
                <a class="w_square me-3 d-flex align-items-center" :href="item.href">
                    <img :src="item.src" :alt="item.text">
                </a>
                <p class="m-0 text-uppercase text-white">{{ item.text }}</p>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use "../../styles/partials/variables";
@use "../../styles/partials/utilities";

div.d-flex {
    a {
        img {
            max-width: 100%;
            max-height: 100%;
            object-fit: contain;
            object-position: center
        }
    }
}
</style>