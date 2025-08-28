<script setup lang="ts">
import chevronUp from './assets/chevron-up-light.svg'
import { ref } from 'vue'

const isOpen = ref(false)
</script>

<template>
  <div class="container">
    <div class="forehead">
      <div class="forehead__badge">
        <h2 class="subtitle-base">Pre-Order</h2>
        <h3 class="subtitle-headline">4510001114</h3>
        <h4 class="caption">#ME11223344</h4>
      </div>
      <div class="column">
        <h5 class="headline-h5-base mb-12">MTP West Buyer</h5>
        <p class="caption mb-4">Jacksonville Group (Jason Burn)</p>
        <p class="caption">jacksonvillegroup@me.com 903-575-3050 999-575-3050</p>
      </div>
      <div class="column forehead__col-right">
        <h5 class="headline-h5-base">USD 20000</h5>
        <p class="headline-h5-base headline-h5-base--success">Need to confirm</p>
        <p class="caption">Created at 2020-04-16 at 15:32:55</p>
      </div>
    </div>
    <div class="card">
      <header class="card__header">
        <p class="card__billing-address caption">Supplier</p>
        <h3 class="semibold card__title">
          <span>Motion Industries INC</span><span class="card__label">#101908</span>
        </h3>
      </header>
      <div class="card__content">
        <div class="column">
          <ul class="card__items">
            <li class="caption">CNPJ: 00.823.053/0001-02</li>
            <li class="caption">
              O Box 1477 - Birmingham AL - 35201-4666 - United States of America
            </li>
            <li class="caption">Jack Jeff Ripple Applejack</li>
          </ul>
        </div>
        <div class="column">
          <ul class="card__items">
            <li class="caption">jack_jeff_applejack@motion.com</li>
            <li class="caption">800-296-5522</li>
            <li class="caption">800-296-5522</li>
            <li class="caption">2020-05-23T12:45:20.39</li>
          </ul>
        </div>
      </div>
    </div>
    <button
      class="headline-h6 button-accordion"
      :class="{ 'button-accordion--is-open': isOpen }"
      @click="isOpen = !isOpen"
    >
      Address
    </button>
  </div>
</template>

<style scoped lang="scss">
@font-face {
  font-family: 'Roboto';
  src: url('/Roboto-Italic-VariableFont_wdth_wght.ttf') format('truetype');
  font-weight: normal;
  font-style: italic;
}

@font-face {
  font-family: 'Roboto';
  src: url('/Roboto-VariableFont_wdth_wght.ttf') format('truetype');
  font-weight: 300;
  font-style: normal;
}
$primary-500-base: #1052e0;
$font-family: 'Roboto', sans-serif;
$neutral-700: #303e49;
$neutral-500-base: #566574;
$system-success-500-base: #1e976c;
$neutral-500-gray-2: #566574;
$neutral-700-gray-0: #303e49;
$primary-50: #edf3ff;

* {
  margin: 0;
  padding: 0;
}

ul {
  list-style: none;
}

.container {
  margin: 0 auto;
  max-width: 85rem;
}

.mb-4 {
  margin-bottom: 0.25rem;
}

.mb-12 {
  margin-bottom: 0.75rem;
}

.subtitle-base {
  font-size: 1.125rem;
  font-weight: 400;
  line-height: 1.5rem;
}

.subtitle-headline {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 2rem;
}

.caption {
  font-size: 0.75rem;
  font-weight: 400;
  line-height: 1rem;
}

.semibold {
  font-size: 0.875rem;
  font-weight: 600;
}

.column {
  display: flex;
  flex-basis: 50%;
  flex-direction: column;
}

.headline-h6 {
  color: $neutral-700;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.25rem;
}

.forehead {
  background: #fff;
  display: flex;
  font-family: $font-family;

  &__badge {
    background-color: $primary-500-base;
    border-radius: 0 0.5rem 0.5rem 0;
    color: #fff;
    margin-right: 1.5rem;
    padding: 1rem;
  }

  &__col-right {
    align-items: flex-end;
    gap: 0.25rem;
  }

  .headline-h5-base {
    color: $neutral-700;
    font-size: 1.25rem;
    font-weight: 600;
    line-height: 1.75rem;

    &--success {
      color: $system-success-500-base;
    }
  }
}
.card {
  box-shadow: 0 0.25rem 0.5rem 0 rgba(0, 0, 0, 0.08);
  font-family: $font-family;
  padding: 1rem;

  &__header {
    display: flex;
    flex-direction: column;
  }

  &__content {
    display: flex;
  }

  &__title {
    align-items: center;
    display: flex;
    gap: 0.5rem;
    margin-bottom: 1rem;
  }

  &__billing-address {
    color: $neutral-500-gray-2;
    margin-bottom: 0.25rem;
  }

  &__label {
    background-color: $primary-50;
    border-radius: 0.5rem;
    color: $primary-500-base;
    display: flex;
    padding: 0.25rem;
  }

  &__items {
    display: flex;
    flex-direction: column;
    gap: 0.25rem;
  }
}

.button-accordion {
  background: transparent;
  border: none;
  display: flex;
  gap: 0.5rem;

  &:before {
    align-items: center;
    background-color: $primary-50;
    background-image: v-bind(chevronUp);
    border-radius: 50%;
    content: '';
    background-repeat: no-repeat;
    background-position: center;
    display: flex;
    height: 1.25rem;
    justify-content: center;
    width: 1.25rem;
  }

  &--is-open:before {
    transform: rotate(180deg);
    transition: transform 0.3s ease;
  }
}
</style>
