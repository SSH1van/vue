<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>
    
<script>
export default {
    name: 'my-button'
}
</script>
    
<style scoped>
.btn {
    padding: 10px 15px;
    border: 1px solid teal;

    color: teal;
    cursor: pointer;
    background: none;
    transition: all linear .25s;
}

.btn:hover {
    color: #fff;
    background-color: teal;
}
</style>