<template>
  <div id="app">
    <hello title="hello hn ui" />
    <hn-layout>
      <hn-toolbar higher>
        <template v-slot:left>
          <hn-icon-group>
            <hn-icon-compose>
              <hn-icon name="hn-ui-icon-query" />
              <hn-icon name="hn-ui-icon-create" />
            </hn-icon-compose>
            <hn-icon name="hn-ui-icon-edit" />
          </hn-icon-group>
        </template>

        <template v-slot:right>
          <hn-icon-group>
            <hn-icon name="hn-ui-icon-help" />
            <hn-icon name="hn-ui-icon-print" />
            <hn-icon name="hn-ui-icon-more" />
          </hn-icon-group>
        </template>
      </hn-toolbar>
      <hn-toolbar-panel>
        <template v-slot:condition>
          <div>Condition</div>
        </template>
        <template v-slot:btn>
          <div>Button</div>
        </template>
      </hn-toolbar-panel>
    </hn-layout>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'App',
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  .hn-ui-layout {
    .hn-ui-icon-group {
      &:before {
        content: '';
      }
    }
  }
}
</style>
