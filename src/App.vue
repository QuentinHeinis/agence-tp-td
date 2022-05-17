<template>

    <div>
        <header class="h-16 border-b border-b-indigo-100 bg-gray-100 w-full flex items-center justify-between px-3">
           <div class="flex items-center">
               <HomeIcon class="w-8 fill-indigo-500"/>
               <span class="font-semibold">Estatery</span>
           </div>
           <div>
               <MenuIcon class="w-8"/>
            </div>
        </header>
        <main class="bg-gray-50  py-14">
            <div class="grid grid-cols-[repeat(auto-fit,minmax(300px,1fr))] w-4/5 mx-auto justify-center gap-7">
            <Card :price="2500" :favori="true" :image="'/public/house2.png'"/>
            <Card :price="2850" :adresse="'2820 Lake Sevilla, Palm Harbor, TX'" :image="'/public/house3.jpg'"/>
            <Card :price="4500" :favori="true" :adresse="'2820 Lake Sevilla, Palm Harbor, TX'" :image="'/public/house.png'"/>
            <Card :price="2850" :adresse="'2820 Lake Sevilla, Palm Harbor, TX'" :image="'/public/house4.jpg'"/>
            <Card :price="2850" :adresse="'2820 Perdu dans la nature'" :image="'/public/house5.jpg'"/>
            <Card :price="2500" :favori="true" :image="'/public/house2.png'"/>
            <Card :price="2850" :adresse="'2820 Lake Sevilla, Palm Harbor, TX'" :image="'/public/house3.jpg'"/>
            <Card :price="4500" :favori="true" :adresse="'2820 Lake Sevilla, Palm Harbor, TX'" :image="'/public/house.png'"/>
            <Card :price="2850" :adresse="'2820 Lake Sevilla, Palm Harbor, TX'" :image="'/public/house4.jpg'"/>
            <Card :price="2850" :adresse="'2820 Lake Sevilla, Perl Harbor, TX'" :image="'/public/house5.jpg'"/>
            </div>
        </main>
        <footer>
            <div class="flex items-center mb-8 mx-16 mt-3">
               <HomeIcon class="w-8 fill-indigo-500"/>
               <span class="font-semibold">Estatery</span>
            </div>
            <div class="flex gap-28 mx-5 pb-16 border-b border-b-indigo-100">
                <div class="flex flex-col gap-3">
                    <div class="flex flex-col">
                        <p class="font-semibold text-base">Sell A Home</p>
                        <span class="text-xs text-gray-400">Request an offer</span>
                        <span class="text-xs text-gray-400">Pricing</span>
                        <span class="text-xs text-gray-400">Reviews</span>
                        <span class="text-xs text-gray-400">Stories</span>
                    </div>
                    <div class="flex flex-col">
                        <p class="font-semibold text-base">Buy A Home</p>
                        <span class="text-xs text-gray-400">Buy</span>
                        <span class="text-xs text-gray-400">Finance</span>
                    </div>
                    <div class="flex flex-col">
                        <p class="font-semibold text-base">Buy, Rent and Sell</p>
                        <span class="text-xs text-gray-400">Buy & sell properties</span>
                        <span class="text-xs text-gray-400">Rent home</span>
                        <span class="text-xs text-gray-400">Builder trade-up</span>
                    </div>
                </div>
                <div class="flex flex-col gap-3">
                    <div class="flex flex-col">
                        <p class="font-semibold text-base">Terms & Privacy</p>
                        <span class="text-xs text-gray-400">Trust & Safety</span>
                        <span class="text-xs text-gray-400">Terms of Service</span>
                        <span class="text-xs text-gray-400">Privacy Policy</span>
                    </div>
                    <div class="flex flex-col">
                        <p class="font-semibold text-base">About</p>
                        <span class="text-xs text-gray-400">Company</span>
                        <span class="text-xs text-gray-400">How it works</span>
                        <span class="text-xs text-gray-400">Contact</span>
                        <span class="text-xs text-gray-400">Investitor</span>
                    </div>
                    <div class="flex flex-col">
                        <p class="font-semibold text-base">Resources</p>
                        <span class="text-xs text-gray-400">Blog</span>
                        <span class="text-xs text-gray-400">Guides</span>
                        <span class="text-xs text-gray-400">FAQ</span>
                        <span class="text-xs text-gray-400">Help Center</span>
                    </div>
                </div>
                
            </div>
            <div class="flex flex-col justify-center items-center gap-2 my-10">
                <span class="text-xs text-gray-400">2021 Estatery. All rights reserved</span>
                <span class="flex items-center gap-4">
                    <insta class="w-4"/>
                    <fb class="w-4"/>
                    <twitter class="w-4"/>
                    <linkedin class="w-5"/>
                </span>
            </div>
        </footer>
    </div>

</template>
 
<script >
import Card from "./components/Card.vue"
import { HomeIcon } from "@heroicons/vue/solid"
import { MenuIcon } from "@heroicons/vue/outline"
import insta from "./components/icones/insta.vue"
import fb from "./components/icones/fb.vue"
import twitter from "./components/icones/twitter.vue"
import linkedin from "./components/icones/linkedin.vue"

export default {
 name: "App",
 components: { Card, HomeIcon, MenuIcon, insta, fb, twitter, linkedin},
};
</script>

