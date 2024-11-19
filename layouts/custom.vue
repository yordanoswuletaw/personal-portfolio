<script setup>
import { useRoute } from 'vue-router';

let theme = useTheme()
const route = useRoute()

const onThemeSwitch = () => {
    theme = useTheme(!theme.value)
}
</script>

<template>
    <div class="min-w-full min-h-full">
        <nav
            class="fixed z-50 bg-gradient-to-r from-primary via-blue-500 to-transparent bg-cover top-0 left-0 right-0 w-full h-14 flex justify-between items-center px-8">
            <div class="flex-1 flex items-center sm:justify-start justify-between">
                <NuxtLink :to="{ name: 'index' }" :class="[route.path === '/' ? 'active-nav' : 'nav']" class="group">Home
                    <div :class="{ 'text-light dark:text-dark': route.path === '/' }"
                        class="absolute text-sm left-[1px] -bottom-[0.45rem] scale-x-0 group-hover:scale-x-100 text-dark dark:text-light transition-all ease-in-out duration-300">
                        ーーー
                    </div>
                </NuxtLink>
                <NuxtLink :to="{ name: 'Projects' }" :class="[route.path.match(/\/projects/i) ? 'active-nav' : 'nav']" class="group">
                    Projects
                    <div :class="{ 'text-light dark:text-dark': route.path.match(/\/projects/i)}"
                        class="absolute text-sm left-[0.5rem] -bottom-[0.6rem] scale-x-0 group-hover:scale-x-100 text-dark dark:text-light transition-all ease-in-out duration-300">
                        ーーー
                    </div>
                </NuxtLink>
                <NuxtLink :to="{ name: 'Feedback' }" :class="[route.path.match(/\/feedback/i) ? 'active-nav' : 'nav']" class="group">
                    Feedback
                    <div :class="{ 'text-light dark:text-dark': route.path.match(/\/feedback/i)}"
                        class="absolute text-sm left-[0.7rem] -bottom-[0.48rem] scale-x-0 group-hover:scale-x-100 text-dark dark:text-light transition-all ease-in-out duration-300">
                        ーーー
                    </div>
                </NuxtLink>
                <button type="button" @click="onThemeSwitch" class="invert">
                    <img v-if="theme" src="~/assets/switch-dark.svg?url" alt="switch dark">
                    <img v-else src="~/assets/switch-light.svg?url" alt="switch light">
                </button>
            </div>

            <div
                :class="[theme ? 'sm:flex hidden md:gap-12 sm:gap-8 items-center invert-0 transition-all ease-in-out duration-300' : 'sm:flex hidden md:gap-12 sm:gap-8 items-center invert transition-all ease-in-out duration-300']">
                <a href="https://www.linkedin.com/in/yordanos-wuletaw/" target="_blank"><img
                        src="~/assets/LinkedIn.svg?url" alt="linkeding" /></a>      
                <a href="https://github.com/yordanoswuletaw" target="_blank"><img src="~/assets/GitHub.svg?url"
                        alt="github" /></a>
                <a href="https://leetcode.com/u/yordanoswuletaw/" target="_blank"><img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIGlkPSJsZWV0Y29kZSI+CiAgPHBhdGggZD0iTTIyLDE0LjM1NWMwLTAuNzQyLTAuNTY0LTEuMzQ2LTEuMjYtMS4zNDZIMTAuNjc2Yy0wLjY5NiwwLTEuMjYsMC42MDQtMS4yNiwxLjM0NnMwLjU2MywxLjM0NiwxLjI2LDEuMzQ2SDIwLjc0QzIxLjQzNiwxNS43MDIsMjIsMTUuMDk4LDIyLDE0LjM1NXoiPjwvcGF0aD4KICA8cGF0aCBkPSJNMy40ODIsMTguMTg3bDQuMzEzLDQuMzYxQzguNzY4LDIzLjUyNywxMC4xMTMsMjQsMTEuNTk4LDI0YzEuNDg1LDAsMi44My0wLjUxMiwzLjgwNS0xLjQ5NGwyLjU4OC0yLjYzN2MwLjUxLTAuNTE0LDAuNDkyLTEuMzY1LTAuMDM5LTEuOWMtMC41MzEtMC41MzUtMS4zNzUtMC41NTMtMS44ODQtMC4wMzlsLTIuNjc2LDIuNjA3Yy0wLjQ2MiwwLjQ2Ny0xLjEwMiwwLjY2Mi0xLjgwOSwwLjY2MnMtMS4zNDYtMC4xOTUtMS44MS0wLjY2MmwtNC4yOTgtNC4zNjNjLTAuNDYzLTAuNDY3LTAuNjk2LTEuMTUtMC42OTYtMS44NjNjMC0wLjcxMywwLjIzMy0xLjM1NywwLjY5Ni0xLjgyNGw0LjI4NS00LjM4YzAuNDYzLTAuNDY3LDEuMTE2LTAuNjQ1LDEuODIyLTAuNjQ1czEuMzQ2LDAuMTk1LDEuODA5LDAuNjYybDIuNjc2LDIuNjA2YzAuNTEsMC41MTUsMS4zNTQsMC40OTcsMS44ODUtMC4wMzhjMC41MzEtMC41MzYsMC41NDktMS4zODcsMC4wMzktMS45MDFsLTIuNTg4LTIuNjM2Yy0wLjY0OS0wLjY0Ni0xLjQ3MS0xLjExNi0yLjM5Mi0xLjMzbC0wLjAzNC0wLjAwN2wyLjQ0Ny0yLjUwM2MwLjUxMi0wLjUxNCwwLjQ5NC0xLjM2Ni0wLjAzNy0xLjkwMWMtMC41MzEtMC41MzUtMS4zNzYtMC41NTItMS44ODctMC4wMzhMMy40ODIsMTAuNDc2QzIuNTA5LDExLjQ1OCwyLDEyLjgxMywyLDE0LjMxMUMyLDE1LjgwOSwyLjUwOSwxNy4yMDcsMy40ODIsMTguMTg3eiI+PC9wYXRoPgo8L3N2Zz4K"
                        alt="leetcode" /></a>
            </div>
        </nav>

        <div class=" min-h-[calc(100vh-3.5rem)] mt-[3.5rem] overflow-hidde flex flex-col">
            <IconsZCurve v-if="['/projects', '/feedback'].includes(route.path.toLocaleLowerCase())"
                class="min-w-full object-cover mt-[1rem]" />

            <div v-if="route.path === '/'" class="xl:-mt-[3rem]  min-w-full relative">
                <IconsUCurve class="xl:mt-[1.5rem]  min-w-full object-cover" />
                <HomeProfile />
                <HomeEndorse />
            </div>

            <div :class="[route.path === '/' ? 'home-bg' : 'other-bg']">
                <slot />
            </div>

            <footer :class="[route.path === '/' ? 'footer-home' : 'footer-other']">
                <div
                    :class="[theme ? 'sm:hidden flex gap-16 items-center invert-0 transition-all ease-in-out duration-300 py-1' : 'sm:hidden flex  items-center invert gap-16 transition-all ease-in-out duration-300 py-1']">
                    <a href="https://www.linkedin.com/in/yordanos-wuletaw/" target="_blank"><img
                            src="~/assets/LinkedIn.svg?url" alt="linkeding" /></a>
                    <a href="https://github.com/yordanoswuletaw" target="_blank"><img src="~/assets/GitHub.svg?url"
                            alt="github" /></a>
                </div>
                <p class="text-xs sm:-order-1 order-2 ">Copyright &copy; {{ (new Date()).getFullYear() }} J0RdN-w. All
                    rights
                    reserved.</p>
                <div class="flex items-center gap-8 text-xs hover:text-primarys">
                    <a href="https://twitter.com/_randomchain" target="_blank" class="flex items-center hover:text-secondary transition-colors ease-in-out duration-300"> <img
                            src="~/assets/tweeter.svg?url" alt="tweeter"> twitter </a>
                    <a href="https://t.me/yordanos219" target="_blank" class="flex items-center hover:text-secondary transition-colors ease-in-out duration-300"> <img
                            src="~/assets/telegram.svg?url" alt="tweeter"> telegram </a>
                </div>
            </footer>
        </div>
    </div>
</template>
