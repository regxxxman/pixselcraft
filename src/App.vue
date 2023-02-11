<script setup>
import HeaderVue from './components/HeaderVue.vue';

import CanvasVue from './components/CanvasVue.vue';

import MainPage from './pages/MainPage.vue';

import Cursor from './components/Cursor.vue';

import { onMounted } from 'vue';
import Cube from './components/Cube.vue';




onMounted(() => {

    ScrollSmoother.create({
        smooth: 1,               // how long (in seconds) it takes to "catch up" to the native scroll position
        effects: true,           // looks for data-speed and data-lag attributes on elements
        smoothTouch: 0.1,        // much shorter smoothing time on touch devices (default is NO smoothing on touch devices)
    });
})
</script>

<template>
    <HeaderVue />

    <Cursor></Cursor>


    <div class="bg flex flex-col min-h-screen ">

        <!-- <CanvasVue class=" absolute w-full" /> -->
        <Cube class="absolute" />



        <div class="flex flex-col lg:flex-row mx-5 lg:space-x-4 pt-16 text-gray-200 my-auto justify-center">

            <div class="basis-1/4">
                <div class="mt-5 p-3 bg-gray-500/25  backdrop-blur-xl rounded-md">
                    <h1 class="font-bold text-2xl"><span class="text-red-500 ">PixselCraft</span> - игровой проект
                        Minecraft.
                    </h1>
                    <p class="text-gray-300 pt-1">Каждый игрок ищет уютную атмосферу и интересный геймплей,
                        отзывчивую
                        модерацию и баланс на сервере. <br>
                        Всё это есть на проекте нового поколения - PixselCraft!
                    </p>
                </div>

                <div class="flex justify-center pt-2">
                    <a
                        class="btn w-full text-center  text-white  bg-cyan-500/25 hover:bg-cyan-500/50 hover:scale-110 ease-out transition backdrop-blur-xl p-2 mr-1 rounded-xl">
                        Войти
                    </a>
                    <a
                        class="btn w-full text-center  text-cyan-500  bg-cyan-900/25 hover:bg-cyan-900/50 hover:scale-110 ease-out transition backdrop-blur-xl p-2 ml-1  rounded-xl">
                        Регистрация
                    </a>

                </div>
            </div>

            <div class="basis-1/2 my-auto flex flex-col space-y-3 pt-5 w-full">
                <h1 class="font-bold text-2xl bg-gray-500/25 backdrop-blur-xl rounded-md p-3">
                    <span class="text-orange-500">Онлайн</span> на наших серверах
                    <p class="text-base text-left font-light ">
                        У наших серверов разные наборы модов и востребованность у игроков
                    </p>
                </h1>
                <div class="pt-2">
                    <div class="pb-1 flex flex-col sm:flex-row sm:space-x-2">
                        <p class="font-bold text-xl z-10"><span class="text-red-500 ">HiTech</span> 45 из 100</p>
                        <div class="flex space-x-2">
                            <span
                                class="py-0.5 px-2 bg-gray-500/25 backdrop-blur-xl rounded-xl  hover:underline decoration-cyan-500"><a
                                    href="">AE2</a></span>
                            <span
                                class="py-0.5 px-2 bg-gray-500/25 backdrop-blur-xl rounded-xl  hover:underline decoration-cyan-500"><a
                                    href="">IndustrialCraft
                                    2</a></span>
                            <span
                                class="py-0.5 px-2 bg-gray-500/25 backdrop-blur-xl rounded-xl  hover:underline decoration-cyan-500">...</span>

                        </div>

                    </div>
                    <div class="w-full bg-gray-500/40 backdrop-blur-xl rounded-full p-1 mt-0.5">
                        <div class=" bg-gradient-to-r  from-green-300 via-blue-500 to-purple-600 animate-text p-2 backdrop-blur-xl text-base font-light text-blue-100 text-center leading-none rounded-full"
                            style="width: 45%"> 45%</div>
                    </div>
                </div>

            </div>
        </div>
    </div>




    <div class="text-white min-h-screen bg2">
        <h1>Новости</h1>
    </div>



</template>

<script>
// import Scrollbar from "vue3-smooth-scrollbar";

// export default {
//     components: { Scrollbar },
// };
</script>

<style lang="sass" scoped>
.bg 
    background: url('../src/assets/BG.jpg') no-repeat
    background-size: 100% 100%


.bg2 
    background: url('../src/assets/bg_site2.jpg') no-repeat
    background-size: 100% 100%

</style>

