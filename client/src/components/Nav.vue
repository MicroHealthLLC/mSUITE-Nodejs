<script setup>
import { storeToRefs } from 'pinia';
import { useAuthStore } from '@/stores';
const authStore = useAuthStore();
const { user } = storeToRefs(authStore);
</script>


<template>
  <v-card>
    <v-layout>
      <v-app-bar prominent v-if="user">
        <router-link to="/" class="no-underline text-dark">
          <img alt="mSuite logo" class="logo ml-15" src="@/assets/images/msuite.png" width="140" />
        </router-link>
        <v-spacer></v-spacer>
        <nav class="mr-5 d-flex">

          <!-- <router-link to="/admin" class="text-dark mr-2 link">
          <v-icon>mdi-folder-wrench-outline</v-icon>
          Admin Panel 
        </router-link> -->

          <!-- <router-link to="/" class="text-dark mr-2 link">
            About
          </router-link>
          
          <router-link to="/" class="text-dark mr-2 link">
            Help
          </router-link>
          <router-link to="/" class="text-dark mr-2 link">
            Terms
          </router-link>
          <router-link to="/" class="text-dark mr-2 link">
            Privacy
          </router-link> -->
          <!--  <span @click="authStore.logout()" class="no-underline text-dark pr-1 cursor">
            <v-icon>mdi-logout</v-icon>
            Logout
          </span> -->
          <!-- <RouterLink to="/profile" class="no-underline text-dark mr-2">
            <v-avatar size="36px">
              <v-img
                v-if="message.avatar"
                alt="Avatar"
                src="https://randomuser.me/api/portraits/women/85.jpg"
              ></v-img>
              <v-icon
                v-else
                :color="message.color"
                :icon="message.icon"
              ></v-icon>            
           
              <v-img src="https://randomuser.me/api/portraits/women/85.jpg" title="Sandra Adams"></v-img>
            </v-avatar>
          </RouterLink> -->


          <a class="nav-link" target="_blank" href="https://github.com/MicroHealthLLC/mSuite/wiki">About</a>

          <a class="nav-link" target="_blank" href="https://github.com/MicroHealthLLC/mSuite/wiki/User-Guide">Help</a>

          <a class="nav-link" target="_blank"
            href="https://github.com/MicroHealthLLC/mSuite/wiki/Terms-of-Service">Terms</a>

          <a class="nav-link" target="_blank"
            href="https://github.com/MicroHealthLLC/mSuite/wiki/Privacy-Policy">Privacy</a>

          <!-- <li class="nav-item" v-if="is_login">
              <a class="nav-link" href="/users/sign_out">Log out</a>
            </li> -->


        </nav>

      </v-app-bar>
      <!-- <v-navigation-drawer
        expand-on-hover
        rail
      >
        <v-list>
            <RouterLink to="/profile" class="no-underline text-dark">
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Sandra Adams"
           
          ></v-list-item>
          </RouterLink>
        </v-list>
      
        <v-divider></v-divider>

        <v-list density="compact" nav>
         <RouterLink to="/admin_panel"  class="no-underline text-dark"> 
            <v-list-item prepend-icon="mdi-folder-wrench-outline" title="Admin Panel" value="myfiles" color="text" class="no-underline"></v-list-item>
        </RouterLink>
          <v-list-item prepend-icon="mdi-help-circle-outline" title="Help" value="shared" color="text" class="no-underline"></v-list-item>
          <v-list-item prepend-icon="mdi-logout" title="Logout" value="starred"  color="text" class="no-underline"></v-list-item>
        </v-list>
      </v-navigation-drawer> -->
      <v-main style="height: 100vh;">
        <RouterView />
      </v-main>
    </v-layout>
  </v-card>
  <!-- <RouterView />  -->
</template>

<style>
.cursor {
  cursor: pointer;
}

a.link {
  color: inherit;
  text-decoration: none;
}
</style>
<!-- <template>
    <nav v-show="authStore.user" class="navbar navbar-expand bg-light">
        <img alt="Vue logo" class="logo ml-3" src="@/assets/images/mh_logo.png" width="165"/>  
        <div class="navbar-nav">
            <router-link to="/" class="nav-item nav-link">Home</router-link>
            <router-link to="/users" class="nav-item nav-link">Users</router-link>
            <button @click="authStore.logout()" class="btn btn-link nav-item nav-link">Logout</button>
        </div>
    </nav>
</template> -->