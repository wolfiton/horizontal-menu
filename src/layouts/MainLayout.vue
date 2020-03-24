<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <HorizontalMenu>
        <template v-slot:h-links>
          <q-list
            v-if="show"
            dense
            bordered
            padding
            class="rounded-borders h-nav"
          >
            <q-item clickable v-ripple>
              <q-item-section>
                Home
              </q-item-section>
            </q-item>
          </q-list>
        </template>
      </HorizontalMenu>
      <q-toolbar>
        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import HorizontalMenu from "components/HorizontalMenu";

export default {
  name: "MainLayout",

  components: {
    HorizontalMenu
  },

  data() {
    return {
      show: true
    };
  },
  methods: {}
};
</script>
