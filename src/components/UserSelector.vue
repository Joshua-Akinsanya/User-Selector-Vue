<template>
    <VSelect
        v-model="selectedUser"
        :items="userList"
        item-title="name"
        item-value="id"
        :return-object="true"
        clearable
        >
        <!--A completer-->
        <template #prepend-item>
            <!--Loader pendant le chargement-->
        </template>

        <template #no-data>
            <!--Aucun utilisateur trouve-->
        </template>
    </VSelect>
</template>

<script setup lang="ts">
import { ref } from 'vue'

interface User {
    id: number;
    name: string;
}

let userList: User[] = [
    {id: 1, name: 'John Maxwell'},
    {id: 2, name: 'Brian Tracy'},
    {id: 3, name: 'Joshua Akinsanya'},
    {id: 4, name: 'Linus Torvalds'},
    {id: 5, name: 'Linus Sebastian'},
]

// Return object set to true in template so type must be User
let selectedUser = ref<User>({id: 0, name: ''});
</script>