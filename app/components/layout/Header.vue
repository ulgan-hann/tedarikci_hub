<template>

  <header
    :class="[
      'fixed left-1/2 -translate-x-1/2 z-[999] transition-all duration-500 ease-in-out',

      isScrolled
        ? 'top-4 w-[96%] max-w-7xl'
        : 'top-0 w-[96%] max-w-7xl'
    ]"
  >

    <!-- GLASS -->
    <div
      :class="[
        isScrolled
          ? 'header-glass'
          : 'bg-white'
      ]"
    >

      <!-- CONTAINER -->
      <div
        :class="[
          'header-container',

          isScrolled
            ? 'px-8 h-24'
            : 'max-w-7xl mx-auto px-6 h-24'
        ]"
      >

        <!-- LEFT -->
        <NuxtLink
          to="/"
          class="flex items-center gap-3 cursor-pointer"
        >

          <img
            src="/img/tedarikcihub_logo.webp"
            alt="TedarikciHub Logo"
            class="w-12 h-12 object-contain" 
          />

          <div>

            <h1 class="text-lg font-bold text-gray-900">
              TedarikciHub
            </h1>

            <p
              class="text-xs uppercase
              tracking-[0.3em] text-gray-400"
            >
              Tedarik Platformu
            </p>

          </div>

        </NuxtLink>

        <!-- DESKTOP NAV -->
        <nav class="hidden lg:flex items-center gap-6">

          <NavLink
            v-for="item in navItems"
            :key="item.title"
            :text="item.title"
            :href="item.href"
          />

        </nav>

        <!-- RIGHT -->
        <NuxtLink to="/basvuru">

          <button
            class="header-button hidden lg:flex"
          >

            <!-- GRADIENT -->
            <span
              class="header-button-gradient"
            ></span>

            <!-- SHINE -->
            <span
              class="header-button-shine"
            ></span>

            <!-- TEXT -->
            <span
              class="header-button-content"
            >
              Hemen Başvur
            </span>

            <!-- ICON -->
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="2"
              stroke="currentColor"
              class="header-button-icon"
            >
              <path
                d="M8 6L8 2L10 2L16 8L10 14L8 14L8 10L0 10L0 6L8 6Z"
              />
            </svg>

          </button>

        </NuxtLink>

        <!-- MOBILE BUTTON -->
        <div
          @click="menuOpen = !menuOpen"
          class="mobile-menu-button flex lg:hidden"
        >

          <!-- HAMBURGER -->
          <svg
            v-if="!menuOpen"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            class="w-7 h-7 text-gray-900"
          >
            <path
              d="M4 6H20M4 12H20M4 18H20"
              stroke="#000000"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>

          <!-- CLOSE -->
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            class="w-7 h-7 text-gray-900"
          >
            <path
              d="M6 6L18 18M18 6L6 18"
              stroke="#000000"
              stroke-width="2"
              stroke-linecap="round"
            />
          </svg>

        </div>

      </div>

    </div>

    <!-- MOBILE MENU -->
    <div
      v-if="menuOpen"
      class="lg:hidden absolute top-24 left-0
      w-full px-6 z-50"
    >

      <div
        class="header-glass
        p-8
        flex flex-col gap-4"
      >

        <NavLink
          v-for="item in navItems"
          :key="item.title"
          :text="item.title"
          :href="item.href"
        />

        <NuxtLink to="/basvuru">

          <button
            class="header-button
            w-full justify-center mt-4"
          >

            <!-- GRADIENT -->
            <span
              class="header-button-gradient"
            ></span>

            <!-- SHINE -->
            <span
              class="header-button-shine"
            ></span>

            <!-- TEXT -->
            <span
              class="header-button-content"
            >
              Hemen Başvur
            </span>

          </button>

        </NuxtLink>

      </div>

    </div>

  </header>

</template>

<script setup>
import {
  ref,
  onMounted,
  onUnmounted
} from 'vue'

import NavLink from '~/components/ui/NavLink.vue'

const menuOpen = ref(false)

const isScrolled = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 30
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

const navItems = [
  {
    title: 'Tedarikçiler',
    href: '/tedarikciler'
  },
  {
    title: 'Hakkımızda',
    href: '/hakkimizda'
  },
  {
    title: 'Tedarikçi Ol',
    href: '/tedarikci-ol'
  },
  {
    title: 'İletişim',
    href: '/iletisim'
  }
]
</script>