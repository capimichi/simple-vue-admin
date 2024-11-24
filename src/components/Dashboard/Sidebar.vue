<template>
  <aside id="sidebar"
         class="absolute left-0 top-0 z-9999 flex h-screen w-72.5 flex-col overflow-y-hidden bg-black duration-300 ease-linear dark:bg-boxdark lg:static lg:translate-x-0 -translate-x-full">
    <div class="flex items-center justify-between gap-2 px-6 py-5.5 lg:py-6.5"><a href="/" class="">
      <img src="https://placehold.co/20x20"/>
    </a>
    </div>

    <div class="no-scrollbar flex flex-col overflow-y-auto duration-300 ease-linear">
      <nav class="mt-5 py-4 px-4 lg:mt-9 lg:px-6">
        <div>
          <h3 class="mb-4 ml-4 text-sm font-medium text-white">MENU</h3>
          <ul class="mb-6 flex flex-col gap-1.5">
            <li v-for="item in menuItems" :key="item.title">
              <nuxt-link :to="item.link"
                         class="flex items-center gap-3.5 px-4 py-2.5 text-sm font-medium text-white rounded-lg hover:bg-gray-700 dark:hover:bg-gray-600">
                <img src="https://placehold.co/20"/>
                <span>{{ item.title }}</span>
              </nuxt-link>
            </li>
          </ul>
        </div>
      </nav>
    </div>
  </aside>
</template>

<script setup lang="ts">

let menuItems = [
  {
    title: 'Dashboard',
    icon: 'home',
    link: '/dashboard'
  },
  {
    title: 'Products',
    icon: 'product-hunt',
    link: '/dashboard/products'
  }
]
</script>