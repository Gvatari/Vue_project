<template>
    <div class="post">
        <div>
            <div>{{ post.id }}</div>
            <div><strong>Название: </strong>{{ post.title }}</div>
            <div><strong>Описание: </strong>{{ post.body }}</div>
        </div>
        <div class="post__btns">
            <my-button
                @click="$emit('remove', post)"
            >
                Удалить
            </my-button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        post: {
            type: Object,
            required: true,
        }
    }
}
</script>

<style scoped>
.post {
    margin: 15px 0 0 0;
    padding: 15px;
    border: 2px solid teal;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>