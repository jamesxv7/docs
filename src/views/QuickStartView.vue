<template lang="pug">
  div(class="view" id="quick-start-view")
    div
      section-def
        dt(slot="title") Getting Started
        dd(slot="desc") Use one of the Vuetify.js Vue CLI packages <em>(based on the official examples)</em> to get your project started in no time. Vuetify.js supports Vue SSR (server-side rendering), SPA (single page application) and standard HTML pages.

    section
      section-header(first) CDN Install
      section-text To test using Vuetify.js without installing a template from Vue CLI, include the files below into your <code>index</code> file of your application after Vue. Vuetify will automatically install and be ready to use.
      markup(lang="html")
        |&lt;link href='https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons' rel="stylesheet" type="text/css"&gt;
        |&nbsp;
        |&lt;link href="https://unpkg.com/vuetify/dist/vuetify.min.css" rel="stylesheet" type="text/css"&gt;
        |&nbsp;
        |&lt;script src="https://unpkg.com/vue/dist/vue.js"&gt;&lt;/script&gt;
        |&nbsp;
        |&lt;script src="https://unpkg.com/vuetify/dist/vuetify.min.js"&gt;&lt;/script&gt;

      h6 Existing Projects
      section-text If you are wanting to use Vuetify in an existing project, you can install by using npm or yarn. Keep in mind, you will still need to <strong><em>include</em></strong> the above css files as they are <strong>not</strong> part of the javascript import.
      markup(lang="cli")
        |$  npm install vuetify --save-dev
        |&nbsp;
        |$  yarn add vuetify --dev
      section-text In your index.js, import Vuetify and apply the plugin to Vue.
      markup(lang="js")
        |import Vue from 'vue'
        |import Vuetify from 'vuetify'
        |&nbsp;
        |Vue.use(Vuetify)
    section
      section-header Vue CLI
      section-text Vuetify has 3 pre-made Vue CLI templates, 2 being forked from <a href="https://github.com/vuejs-templates" target="_blank">official Vue.js templates</a>. They contain small modifications to help you get started with Vuetify even faster. These packages require <code>vue-cli</code>. For more information on vue-cli, visit the official <a href="https://github.com/vuejs/vue-cli" target="_blank">Github</a> repository.
      v-tabs(class="elevation-1 mb-5" grow icons)
        v-tab-item(ripple slot="activators" href="#simple") Simple HTML
          v-icon accessibility
        v-tab-item(ripple slot="activators" href="#webpack") Webpack
          v-icon web
        v-tab-item(ripple slot="activators" href="#webpack-ssr") Webpack SSR
          v-icon cloud_circle
        v-tab-item(ripple disabled slot="activators" href="#nuxt") NUXT (coming soon)
          v-icon business
        v-tab-content(id="simple" slot="content")
          v-card
            v-card-text
              h4 Simple HTML Quick Start
              p This template is intended for users who want to try out Vue.js and Vuetify.js in the most simplistic way. It contains a basic index.html with no additional functionality. This is useful for developers who want to easily preview the features of the framework.
              markup(lang="cli")
                |$  vue init vuetifyjs/simple
        v-tab-content(id="webpack" slot="content")
          v-card
            v-card-text
              h4 Webpack Quick Start
              p This template is intended for users who are already familiar with Vue/Webpack. It contains a very simple webpack setup and is targetted at developers creating prototype or basic applications.
              markup(lang="cli")
                |$  vue init vuetifyjs/webpack
        v-tab-content(id="webpack-ssr" slot="content")
          v-card
            v-card-text
              h4 Webpack SSR Quick Start
              p This template is for advanced users looking to utilize the new Vue SSR (server-side rendering). Based off of the structure in the Vue.js 2 <a href="https://github.com/vuejs/vue-hackernews-2.0" target="_blank">Hackernews</a> repository. The Vuetify.js SSR template provides next generation functionality for advanced Vue applications.
              markup(lang="cli")
                |$  vue init vuetifyjs/webpack-ssr
      p If you are using the <strong>Simple HTML</strong> template, you are ready to go. Open the <code>index.html</code> in any browser to get started.
      h6 NPM Install
      section-text After the vue-cli installation finishes, <kbd>cd</kbd> into your project directory and type <kbd>npm install</kbd>. Alternatively, if you are using Facebook's recently released <a href="https://yarnpkg.com/" target="_blank">yarn package manager</a>, you can simply type <kbd>yarn</kbd>.

      section-text Once the package installation is complete, type <kbd>npm run dev</kbd> into your console. This will start a <a href="https://nodejs.org/en/" target="_blank">nodejs</a> server locally which can be accessed by navigating to <a href="http://localhost:8080" target="_blank">http://localhost:8080</a> in your browser.
    section
      whats-next(route="/style/theme" text="Theme") Now that you have your project ready to go, it's time to setup a custom theme.
</template>

<script>
  export default {
    mounted () {
      this.$emit('view', this.meta())
    },

    preFetch () {
      return this.methods.meta()
    },

    methods: {
      meta () {
        return {
          title: 'Quick Start | Vuetify.js',
          h1: 'Quick Start',
          description: 'Get started with Vue and Vuetify in no time.',
          keywords: 'vuetify quick start, vuetify templates, server side rendering'
        }
      }
    }
  }
</script>
