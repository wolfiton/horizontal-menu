<template>
  <div>
    <span>
      <q-btn
        flat
        dense
        round
        icon="menu"
        aria-label="Menu"
        @click="show = !show"
        label="Menu"
      />

      <transition name="hmenu">
        <slot name="h-links">
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

            <q-item clickable v-ripple>
              <q-item-section>
                About
              </q-item-section>
            </q-item>

            <q-item clickable v-ripple>
              <q-item-section>
                Comment
              </q-item-section>
            </q-item>
          </q-list>
        </slot>
      </transition>
    </span>
  </div>
</template>

<script>
export default {
  name: "HorizontalMenu",
  data() {
    return {
      show: true
    };
  },
  props: {
    icon: {
      type: String,
      default: ""
    },
    lorem: {
      type: String,
      default: "A simple card"
    }
  },
  methods: {
    ClickMe() {
      console.log("I am clicked");
    }
  }
};
</script>

<style scoped>
.h-nav {
  display: flex;
  flex-direction: row;
}
</style>
