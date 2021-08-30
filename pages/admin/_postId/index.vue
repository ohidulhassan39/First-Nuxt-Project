<template>
    <div class="admin-post-page">
        <section class="update-form">
            <AdminPostForm :post="loadedPost" />
        </section>
    </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm'

export default {
    layout: 'admin',
    components: {
        AdminPostForm
    },
    data() {
        return {
            loadedPost: {
                author: 'Ohidul hassan',
                title: 'My First Post',
                content: 'Super amazing, Thanks for that!!!!',
                thumbnailLink: 'https://images.pexels.com/photos/2058853/pexels-photo-2058853.jpeg',
            }
        }
    }
}
</script>

<style scoped>
    .update-form {
        width: 90%;
        margin: 10px auto;
    }

    @media (min-width: 768px) {
        .update-form {
            width: 600px;
        }
    }
</style>