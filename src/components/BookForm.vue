<template>
    <form action="#" method="post" @submit.prevent="bookSubmit(bookTitle,bookAuthor)">
        <input type="text" name="title" v-model="bookTitle" placeholder="Book Title">
        <input type="text" name="author" v-model="bookAuthor" placeholder="Book Author">
        <button type="submit" name="button">Add Book</button>
    </form>
</template>

<script>
    export default {
        name: 'BookForm',
        props: ['books'],
        data() {
            return {
                bookTitle: '',
                bookAuthor: '',
            }
        },
        methods: {
            bookSubmit(bookTitle, bookAuthor) {
                this.$emit('addBook', bookTitle, bookAuthor);
            }
        },
    }
</script>

<style scoped>

</style>