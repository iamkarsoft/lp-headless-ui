
<template>
  <div class="min-h-screen bg-gray-200 text-gray-900">
    <div class="container px-4">
      <h2 class="font-bold text-xl pt-2">Menu (dropdown)</h2>
      <Menu>
    <MenuButton class="flex items-center bg-blue-500 text-white rounded-md px-4 py-2">

      <span>More</span>
      <ChevronDownIcon class="h-5 w-5 ml-2" />
    </MenuButton>
    <MenuItems class="absolute bg-white  shadow-md rounded-lg flex flex-col focus:outline-none w-56 mt-2">
      <MenuItem  v-slot="{ active }">
        <a clas="flex items-center rounded-md px-2 py-2"  :class='{ "bg-blue-500 text-white": active }' href="/account-settings">
          <ArrowRightIcon class="h-4 w-4" />
          <span class="ml-2">Account settings</span>
        </a>
      </MenuItem>
      <MenuItem  v-slot="{ active }">
        <a :class='{ "bg-blue-500": active }' href="/account-settings">
          Documentation
        </a>
      </MenuItem>
      <MenuItem  disabled>
        <span class="opacity-75">Invite a friend (coming soon!)</span>
      </MenuItem>
    </MenuItems>
  </Menu>
    </div>
  </div>

</template>

<script >
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";
import { ChevronDownIcon, ArrowRightIcon } from '@heroicons/vue/solid'
  export default {
    components: {
      Menu,
      MenuButton,
      MenuItems,
      MenuItem,
      ChevronDownIcon,
      ArrowRightIcon
    },
  };
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
};
</style>
