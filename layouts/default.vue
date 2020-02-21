<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app flat color="#FFFFFF">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
       <v-toolbar-title>
          <v-img  src="/logo.svg" height="50px" width="120px">
          </v-img>
       </v-toolbar-title>
      
         
        
        <v-spacer />
        <hr>
            <v-icon class="mr-3" large color="green darken-2">mdi-magnify</v-icon>
               <v-btn
        depressed
        >
             <v-badge
          color="#007BFF"
          content="6"
          overlap
        >
     
          <v-icon  large color="green darken-2">mdi-email-outline</v-icon>
          </v-badge>
          Messages
        </v-btn>

                  <v-btn
        depressed
        >
             <v-badge
          color="#007BFF"
          content="6"
          overlap
        >
     
          <v-icon class="mr-3" large color="green darken-2">mdi-cart-outline</v-icon>
          </v-badge>
          Market place
        </v-btn>

           <v-btn
        depressed
        >
             <v-badge
          color="#007BFF"
          content="6"
          overlap
        >
     
          <v-icon class="mr-3" large color="green darken-2">mdi-menu</v-icon>
          </v-badge>
          Notifications
        </v-btn>
        
         <v-avatar>
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>
    <div>
      Me
    </div>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-footer :fixed="fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
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
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js"
    };
  }
};
</script>
