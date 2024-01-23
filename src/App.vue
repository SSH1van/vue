<template>
    <div class="container">
        <post-form @create="createPost" />
        <post-list :posts="posts" @remove="removePost"/>
    </div>
</template>


<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
    components: {
        PostForm, PostList
    },
    data() {
        return {
            posts: [
                { id: 1, title: 'Javascript 1', body: 'Описание поста 1' },
                { id: 2, title: 'Javascript 2', body: 'Описание поста 2' },
                { id: 3, title: 'Javascript 3', body: 'Описание поста 3' },
            ]
        }
    },
    methods: {
        createPost(post) {
           this.posts.push(post);
        },
        removePost(post) {
            this.posts = this.posts.filter(p => p.id !== post.id)

        }
    }
}   
</script>


<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}
</style>