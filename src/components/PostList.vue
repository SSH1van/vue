<template>
    <div v-if="posts.length > 0">
        <h3>Интересные выпуски</h3>
        <post-item v-for="post in posts" :post="post" :key="post.id" @remove="$emit('remove', post)"/>
    </div>
    <h3 style="color:red" v-else>Список постов пуст</h3>
    
        
</template>
    
<script>
import PostItem from "@/components/PostItem.vue"
export default {
    components: {PostItem},
    props: {
        posts: {
            type: Array,
            required: true,
        }
    }
}
</script>
    
<style scoped>

</style>