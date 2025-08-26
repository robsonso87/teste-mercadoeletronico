<script setup lang="ts"></script>

<template>
  <div class="container">
    <div class="forehead">
      <div class="forehead__badge">
        <h2 class="subtitle-base">Pre-Order</h2>
        <h3 class="subtitle-headline">4510001114</h3>
        <h4 class="caption">#ME11223344</h4>
      </div>
      <div class="forehead__col">
        <h5 class="headline-h5-base mb-12">MTP West Buyer</h5>
        <p class="caption mb-4">Jacksonville Group (Jason Burn)</p>
        <p class="caption">jacksonvillegroup@me.com 903-575-3050 999-575-3050</p>
      </div>
      <div class="forehead__col forehead__col--right">
        <h5 class="headline-h5-base">USD 20000</h5>
        <p class="headline-h5-base headline-h5-base--success">Need to confirm</p>
        <p class="caption">Created at 2020-04-16 at 15:32:55</p>
      </div>
    </div>
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

* {
  margin: 0;
  padding: 0;
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

  &__col {
    display: flex;
    flex-basis: 50%;
    flex-direction: column;

    &--right {
      align-items: flex-end;
      display: flex;
      gap: 0.25rem;
    }
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
</style>
