<template>
    <nav class="border-b bg-gray-900 border-gray-700 w-full top-0 left-0 z-50">
        <div class="container px-4 py-5 mx-auto space-y-4 lg:space-y-0 lg:flex lg:items-center lg:justify-between lg:space-x-10">
            <div class="flex justify-between">
                <nuxt-link to="/" class="text-gray-200 font-semibold">
                    QRCODE
                </nuxt-link>
            </div>
            <div id="nav" class="flex flex-col lg:flex-row items-center lg:justify-between flex-1 space-x-2">
                <div class="flex flex-col space-y-4 lg:space-y-0 lg:flex-row lg:space-x-6 xl:space-x-8 justify-center items-center mb-12 lg:mb-0">
                    <nuxt-link to="/" class="navlink">Home</nuxt-link>
                    <nuxt-link to="/about" class="navlink">About</nuxt-link>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name:'navbar'
}
</script>