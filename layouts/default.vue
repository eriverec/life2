<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :clipped="clipped"
      fixed
      app
      absolute
      temporary
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      
      
      <v-toolbar-title v-text="title" />
      <v-spacer />
      
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <Footer />
 
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        },
        {
          title: "Campos",
          to: "/camp"
        },
        {
          title: "Educación",
          to: "/educ"
        },
        {
          title: "Experiencia",
          to: "/exp"
        },
        {
          title: "Referencias",
          to: "/refer"
        },
        {
          title: "Conocimientos",
          to: "/conoc"
        }
      ],

      title: "LIFE dos"
    };
  }
};
</script>
