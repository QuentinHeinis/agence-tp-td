<template>

    <div>
        <header class="h-16 border-b border-b-indigo-100 bg-gray-100 w-full px-3 sticky top-0 z-40">
           <div class="flex items-center justify-between w-full h-full">
                <div class="flex items-center">
                    <HomeIcon class="w-8 fill-indigo-500"/>
                    <span class="font-semibold">Estatery</span>
                </div>
                <div class="lg:hidden">
                    <MenuIcon class="w-8 cursor-pointer" @click="MenuOpen=!MenuOpen"/>
                </div>
                <nav class="absolute bg-slate-300 w-full left-0 top-16 pl-2 -translate-y-[200%] lg:translate-y-0 lg:relative lg:top-0 lg:bg-transparent lg:w-fit" 
                :class="MenuOpen && 'translate-y-0'">
                    <ul class="flex flex-col py-4 gap-8 lg:flex-row">
                        <li>Rent</li>
                        <li>Buy</li>
                        <li>Sell</li>
                        <li>Manage Property</li>
                        <li>Ressources</li>
                    </ul>
                </nav>
           </div>
        </header>
        <main class="bg-gray-50  py-14 px-4 font-inter">
            <div class="flex-col flex mx-auto w-4/5 gap-7 mb-7">
                <div class="flex flex-col gap-7 lg:flex-row lg:justify-between">
                <h2 class="text-center text-4xl text-indigo-900 font-bold">Search properties to rent</h2>
                <div class="flex items-center">
                    <input type="search" placeholder="Search with Search Bar" class="placeholder:text-xs h-12 px-4 rounded-lg border-2 w-full border-indigo-100">
                    <ChevronDownIcon class="w-5 h-5 -ml-8 bg-indigo-100 stroke-indigo-600 p-1 rounded-full"/>
                </div>
                    
                </div>
                <div class="flex items-center lg:hidden">
                    <input type="search" placeholder="Search Location" class="placeholder:text-xs h-16 px-4 rounded-lg border-2 w-full border-indigo-100">
                    <SearchIcon class="w-10 h-10 -ml-12 bg-indigo-600 stroke-indigo-100 p-1 rounded-sm"/>
                </div>
                <div class="hidden items-center lg:flex h-24 px-4 rounded-lg border-2 w-full border-indigo-100 font-inter gap-4">
                    <div class="px-4 border-r-2 border-gray-300 min-w-max w-1/2">
                        <span class="text-base text-gray-900">Location</span>
                        <p class="text-lg font-bold">New York, USA</p>
                    </div>
                    <div class="px-4 border-r-2 border-gray-300 min-w-max w-1/2">
                        <span class="text-base text-gray-900">When</span>
                        <p class="text-lg font-bold">Select Move-in Date</p>
                    </div>
                    <div class="px-4 pr-10 border-r-2 border-gray-300 min-w-max w-1/2">
                        <span class="text-base text-gray-900">Price</span>
                        <p class="text-lg font-bold">$500-$2,500</p>
                    </div>
                    <div class=" flex items-center justify-center w-1/2">
                        <p class="text-center bg-indigo-600 px-6 py-3 rounded-sm text-indigo-100">Search</p>
                    </div>
                </div>
            </div>
            <div class="grid grid-cols-[repeat(auto-fit,minmax(300px,1fr))] w-4/5 mx-auto justify-center gap-7">
                <Card :price="2500" :favori="true" :image="'./assets/house2.png'"/>
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
        <footer >
            <div class="flex flex-col lg:flex-row pt-4">
                <div class="flex items-center mb-8 mx-16 mt-3">
               <HomeIcon class="w-8 fill-indigo-500"/>
               <span class="font-semibold">Estatery</span>
            </div>
            <div class="flex gap-28 mx-5 pb-16  lg:flex-col w-full">
                <div class="flex flex-col gap-3 lg:flex-row lg:w-full lg:justify-around">
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
                <div class="flex flex-col gap-3 lg:flex-row lg:w-full lg:justify-around">
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
            </div>
            <div class="flex flex-col justify-center items-center gap-2 my-10 border-t border-t-indigo-100 pt-10 lg:flex-row">
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
import { MenuIcon, ChevronDownIcon, SearchIcon } from "@heroicons/vue/outline"
import insta from "./components/icones/insta.vue"
import fb from "./components/icones/fb.vue"
import twitter from "./components/icones/twitter.vue"
import linkedin from "./components/icones/linkedin.vue"

export default {
 name: "App",
 components: { Card, HomeIcon, MenuIcon, insta, fb, twitter, linkedin, ChevronDownIcon, SearchIcon},
 data(){
     return{
         MenuOpen:false,
     }
 },

};
</script>

