<template>
    <div class="list">
        <li class="list-item"
            :key="user.id"
            v-for="user in users"

        >
            {{ user.name }}
        </li>
    </div>
</template>
<script lang="ts">
import {defineComponent} from 'vue'
import {useUsers} from '@/use/users'
export default defineComponent({
    async setup(){
        const { users } = await useUsers()
        users.value!.map(user => {
            user
        })
        return {
            users
        }
    }
})
</script>