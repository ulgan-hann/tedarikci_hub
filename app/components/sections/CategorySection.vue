<template>

  <section class="section-spacing">

    <div class="page-container">

      <!-- TOP -->
      <div
        class="flex flex-col
        items-center text-center"
      >

        <!-- BADGE -->
        <div class="hero-badge">

          <div class="hero-badge-dot"></div>

          <span>
            Tedarikçi kategorileri
          </span>

        </div>

        <!-- TITLE -->
        <h2
          class="section-title
          mt-8 max-w-5xl"
        >
          13 sektörde uçtan uca tedarik.
        </h2>

        <!-- DESCRIPTION -->
        <p
          class="section-description
          mt-8"
        >
          Tüm kategorileri görüntülemek için
          aşağıdaki barı açın —
          her kategori sektör uzmanları
          tarafından özenle seçilir.
        </p>

      </div>

      <!-- CATEGORY BOX -->
      <div
        class="
        category-box
        mt-20
        "
      >

        <!-- HEADER -->
        <button
          @click="isOpen = !isOpen"
          class="category-header"
        >

          <!-- LEFT -->
          <div class="flex items-center gap-4">

<div class="category-item-icon">

  <svg
    xmlns="http://www.w3.org/2000/svg"
    fill="none"
    viewBox="0 0 24 24"
    stroke-width="2"
    stroke="currentColor"
    class="w-6 h-6 text-gray-900"
  >
    <path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M4 4h6v6H4V4zm10 0h6v6h-6V4zM4 14h6v6H4v-6zm10 0h6v6h-6v-6z"
    />
    
  </svg>

</div>

            <div class="text-left">

              <h3 class="category-header-title">
                Tüm sektörler
              </h3>

<p class="category-header-description">
  13 kategori —
  {{ isOpen
    ? 'daraltmak için tıklayın'
    : 'açmak için tıklayın'
  }}
</p>

            </div>

          </div>

          <!-- RIGHT -->
          <div class="category-header-right">

            <div class="category-count hidden md:flex">
              2.550+ tedarikçi
            </div>

            <div
              :class="[
                'transition-transform duration-500',
                isOpen ? 'rotate-180' : ''
              ]"
            >
              ▼
            </div>

          </div>

        </button>

        <!-- CONTENT -->
<!-- CONTENT -->
<Transition name="category-expand">

  <div
    v-show="isOpen"
    class="category-content-wrapper"
  >

    <div class="category-grid">

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          👕

        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Tekstil ve Konfeksiyon
          </h4>

          <p class="category-item-description">
            482 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🧴
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Kozmetik ve Kişisel Bakım
          </h4>

          <p class="category-item-description">
            213 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🍽️
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Gıda ve İçecek
          </h4>

          <p class="category-item-description">
            376 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          📦
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Ambalaj
          </h4>

          <p class="category-item-description">
            168 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🛋️
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Mobilya ve Ev
          </h4>

          <p class="category-item-description">
            241 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          ⚙️
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Endüstriyel Ürünler
          </h4>

          <p class="category-item-description">
            198 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🧪
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Kimyasallar
          </h4>

          <p class="category-item-description">
            96 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🚗
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Otomotiv
          </h4>

          <p class="category-item-description">
            132 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🧼
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Temizlik Ürünleri
          </h4>

          <p class="category-item-description">
            87 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🎁
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Promosyon Ürünleri
          </h4>

          <p class="category-item-description">
            121 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🏗️
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            İnşaat Malzemeleri
          </h4>

          <p class="category-item-description">
            173 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          🔩
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Makine
          </h4>

          <p class="category-item-description">
            109 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

      <!-- ITEM -->
      <div class="category-item">

        <div class="category-item-icon">
          💻
        </div>

        <div class="category-item-content">

          <h4 class="category-item-title">
            Elektronik
          </h4>

          <p class="category-item-description">
            143 doğrulanmış tedarikçi
          </p>

        </div>

      </div>

    </div>

    <!-- FOOTER -->
    <div class="category-footer">

      Tüm tedarikçileri dizinde inceleyin.

    </div>

  </div>

</Transition>

      </div>

    </div>

  </section>

</template>

<script setup>

import { ref, onMounted } from 'vue'

const isOpen = ref(false)

onMounted(() => {

  isOpen.value = window.innerWidth > 1024

})

</script>