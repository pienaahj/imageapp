<script lang="ts" setup>
    // import { defineEmits } from 'vue';

    const emits = defineEmits(['selectOption']);

    const selectOption = (isColor: boolean) => {
        emits("selectOption", isColor);
    };
</script>

<template>
    <v-navigation-drawer
        expand-on-hover
        rail
    >
        <v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Sandra Adams"
            subtitle="sandra_a88@gmailcom"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
            <v-list-item 
                prepend-icon="mdi-image" 
                title="Color Gallery" 
                value="color"
                @click="selectOption(true)"
            >
            </v-list-item>
            <v-list-item
                prepend-icon="mdi-dialpad" 
                title="Gray Space Gallery" 
                value="gray"
                @click="selectOption(false)"
                >
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>