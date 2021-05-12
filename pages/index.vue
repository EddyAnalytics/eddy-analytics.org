<template>
  <main>
    <section class="hero hero is-medium-with-navbar is-primary is-bold">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title">
            <img
              class="hero__logo"
              src="@/assets/img/logo-brand-white.svg"
              alt="Eddy Logo"
            />
          </h1>
          <h1 class="subtitle p-t-md p-b-md">
            Open-source unified data analytics platform
          </h1>
        </div>
      </div>
    </section>

    <section id="instructions" class="section is-light">
      <div class="container">
        <div class="columns is-centered is-vcentered has-text-centered">
          <div class="column">
            <figure class="image is-square">
              <img
                src="@/assets/img/illustrations/deploy.svg"
                class="instructions__image"
                alt="Movie Night Illustration"
              />
            </figure>
            <p class="is-size-5 has-text-weight-semibold">
              Deploy the platform on any
              <a href="https://kubernetes.io/" target="_blank">Kubernetes</a>
              cluster and use computation power from public cloud, hybrid or
              on-premises servers.
            </p>
          </div>
          <div class="column">
            <figure class="image is-square">
              <img
                src="../assets/img/illustrations/pipelines.svg"
                class="instructions__image"
                alt="Create pipelines"
              />
            </figure>
            <p class="is-size-5 has-text-weight-semibold">
              Architecture advanced data pipelines by using a visual builder,
              transformation blocks, and various data sources and sinks
            </p>
          </div>
          <div class="column">
            <figure class="image is-square">
              <img
                src="../assets/img/illustrations/dashboards.svg"
                class="instructions__image"
                alt="Dashboards"
              />
            </figure>
            <p class="is-size-5 has-text-weight-semibold">
              Create and present real-time dashboards containing visualisation
              based on the output of the data pipelines
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="motivation" class="section is-medium has-background-white-bis">
      <div class="container">
        <div class="columns is-vcentered">
          <div class="column is-5">
            <h2 class="title is-size-2 is-spaced">
              Unified analytics for everyone
            </h2>
            <p class="is-size-5">
              The existing unified data analytics platforms consist of either
              proprietary technologies or managed solutions deployed on cloud
              infrastructure offered by the big cloud providers. We believe that
              the creation of a data analytics platform which can be deployed on
              any infrastructure represents a valuable addition to the
              open-source community. Our platform is architectured in such a way
              that it can be deployed to a Kubernetes cluster which can run
              on-premises, on public cloud or hybrid eliminating the vendor
              lock-in imposed by the existing solutions.
            </p>
            <br />
            <br />
            <div class="has-text-centered">
              <b-button
                size="is-medium"
                icon-right="github"
                @click="goToOrganization()"
              >
                View on GitHub
              </b-button>
              <b-button
                size="is-medium"
                type="is-primary"
                @click="goToDemoApp()"
              >
                Try our demo
              </b-button>
            </div>
          </div>
          <div class="column is-offset-1 is-6">
            <figure class="image is-3by2">
              <img
                src="../assets/img/illustrations/data-platform.svg"
                class=""
                alt="Unified analytics platform"
              />
            </figure>
          </div>
          <br />
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      ORGANIZATION_URL: 'https://github.com/EddyAnalytics',
      DEMO_APP_URL: 'https://app.eddy-analytics.org/auth',
    }
  },
  methods: {
    goToOrganization() {
      window.open(this.ORGANIZATION_URL, '_blank')
    },
    goToDemoApp() {
      window.open(this.DEMO_APP_URL, '_blank')
    },
  },
}
</script>

<style lang="scss" scoped>
#instructions {
  .instructions__image {
    margin: 0 auto;
    max-width: 60%;
  }
}
</style>
