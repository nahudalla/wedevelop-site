<template>
  <div class="services" id="services">
    <h2>What we do</h2>
    <ul class="service-list">
      <Service v-for="service in services" v-bind:key="service.id" v-bind:service="service" />
    </ul>
  </div>
</template>

<script>
import Service from './Service.vue'

export default {
  name: 'Services',
  components: {
    Service
  },
  data: function () {
    return {
      services: [
        {
          id: 1,
          name: 'Web Development',
          description: 'From basic institutional webpages to large Web Applications, we create solutions <span class="highlight-paragraph">focused on scalability, performance, and user experience.</span>',
          photo: require('../assets/img/t.svg')
        },
        {
          id: 2,
          name: 'Consulting Services',
          description: 'Our extensive experience allows us to help you with decisions regarding your daily work. We help you to <span class="highlight-paragraph">find improvement opportunities</span> and to make your software or your software development process better.',
          photo: require('../assets/img/c.svg')
        },
        {
          id: 3,
          name: 'Outsourcing',
          description: 'We provide <span class="highlight-paragraph">the human resources you need</span>, either an entire and independent team or specific professionals for your projects.',
          photo: require('../assets/img/u.svg')
        }
      ]
    }
  }
}
</script>

<style scoped>
  h2 {
    margin: 0 0 1.8em 0;
    color: #272A40;
    font-size: 50px;
    font-weight: 900;
    letter-spacing: 1px;
    line-height: 60px;
  }

  .services {
    margin-top: 8.5em;
  }

  .service-list {
    display: flex;
    flex-wrap: wrap;
    padding: 0 7em;
    margin: 0;
    list-style-type: none;
  }

  @media (max-width: 1400px) {
    .service-list {
      padding: 0 5em;
    }
  }

  @media (max-width: 1200px) {
    h2 {
      font-size: 40px;
    }
  }

  @media (max-width: 576px) {
    h2 {
      margin: 0 0 2.7em 0;
      font-size: 30px;
      letter-spacing: 0.6px
    }

    .services {
      margin-top: 5em;
    }

    .service-list {
      flex-direction: column;
      padding: 0 1.6em;
    }
  }
</style>
