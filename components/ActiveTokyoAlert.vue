<template>
  <span class="linkButton">
    <antenna-icon aria-hidden="true" class="svgIcon" />
    <span class="text">
      {{ $t('医療非常事態宣言発令中') }}
    </span>
  </span>
</template>

<script lang="ts">
import Vue from 'vue'

import AntennaIcon from '@/static/antenna.svg'

export default Vue.extend({
  components: {
    AntennaIcon,
  },
})
</script>

<style lang="scss" scoped>
.linkButton {
  background-color: $alert;
  border: 2px solid $alert;
  color: $white;
  border-radius: 3em;
  padding: 4px 8px;
  margin-right: 8px;
  display: inline-flex;
  font-weight: bold;
  @include font-size(14);

  .svgIcon {
    fill: #fff;
  }

  &:hover {
    background-color: $white;
    color: $alert;
    .svgIcon {
      fill: $alert !important;
    }
  }

  .textLink {
    display: flex;
    align-items: center;
    color: $white !important;
    text-decoration: none;
    margin: -10px;
    padding: 10px;
    i {
      color: inherit;
    }
    &:hover {
      color: $alert !important;
    }
  }

  .text {
    margin: 0 4px;
  }

  @include lessThan($medium) {
    margin-top: 8px;
  }
}
</style>
