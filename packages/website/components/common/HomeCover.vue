<template>
  <section
    :style="
      `background-image: url(${require('~/assets/img/dividers/inclined-line.svg')});`
    "
    class="h-full bg-bottom bg-repeat-x pt-2 pb-8 bg-white"
  >
    <div class="container">
      <div
        class="flex flex-wrap items-center justify-center text-center lg:text-left"
      >
        <div class="w-full lg:w-1/3 pb-4 lg:pr-4">
          <h1
            class="text-3xl sm:text-4xl font-semibold leading-none mb-4"
          >
            {{ $t('slogan') }}
          </h1>
          <h2
            class="text-lg sm:text-xl text-blue-darker font-normal leading-normal mb-2"
            v-html="$t('description')"
          />
          <div
            class="flex flex-col sm:flex-row justify-center lg:justify-start pt-8"
          >
            <a
              :href="$t('links.getStarted.url')"
              class="btn btn-blue mb-2 sm:mb-0 sm:mr-2"
            >
              {{ $t('links.getStarted.title') }}
            </a>
            <button
              v-scroll-to="'#features'"
              class="btn btn-grey mt-2 sm:mt-0 sm:ml-2"
            >
              {{ $t('links.learnMore.title') }}
            </button>
          </div>
        </div>
        <div class="w-full lg:w-2/3 pb-4 lg:pl-4 z-20">
          <div v-lazy-container="{ selector: 'img' }">
            <img
              :title="$t('slogan')"
              :data-src="require(`~/assets/img/home-cover/home-cover-${$i18n.locale}.jpg`)"
              :data-srcset="`${require(`~/assets/img/home-cover/home-cover-${$i18n.locale}.jpg`)} 1x, ${require(`~/assets/img/home-cover/home-cover-${$i18n.locale}@2x.jpg`)} 2x`"
              src="~assets/img/home-cover/home-cover-loading.svg"
              alt="Statusfy"
              class="rounded shadow"
              width="1027"
              height="697">
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  background-size: 100% 100px;
}
</style>
