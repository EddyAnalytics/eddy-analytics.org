<template>
  <div>
    <b-navbar fixed-top>
      <template #brand>
        <b-navbar-item tag="router-link" :to="{ name: 'index' }">
          <img
            src="@/assets/img/logo-brand.svg"
            alt="Eddy Data Analytics logo"
          />
        </b-navbar-item>
      </template>
      <template #start></template>
      <template #end>
        <b-button type="is-primary" class="m-2" @click="goToDemoApp()">
          Try our demo
        </b-button>
      </template>
    </b-navbar>
    <nuxt />
    <footer class="footer">
      <div class="container">
        <div class="columns is-vcentered">
          <div class="column">
            <div>Partners</div>
            <a href="https://www.elnino.tech" target="_blank">
              <img
                src="@/assets/img/elnino-logo-white.svg"
                alt="El Niño"
                title="El Niño"
                height="50"
                width="150"
              />
            </a>
          </div>
          <div class="column has-text-right">
            &copy; {{ new Date().getFullYear() }} Eddy Analytics
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      DEMO_APP_URL: 'https://app.eddy-analytics.org/auth',
    }
  },
  methods: {
    goToDemoApp() {
      window.open(this.DEMO_APP_URL, '_blank')
    },
  },
}
</script>

<style lang="scss" scoped>
.navbar {
  box-shadow: 0 2px 0 0 whitesmoke;

  .navbar-item.is-active {
    font-weight: 500;
  }
}
.footer {
  flex: 1;
}
</style>
