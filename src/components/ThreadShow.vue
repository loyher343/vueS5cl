<template>
    <div>
        <h1>Tis better to vie than vie esteem</h1>
    </div>
</template>

<script>

    import sourceData from '@/data'

    export default {
        props:{
            id: {
                required: true,
                // type: string
            }
        },
        data () {
            console.log(this)
            return{
                thread: sourceData.threads[this.id],
                posts: sourceData.posts,
                users: sourceData.users
            }
        }
    }

</script>
