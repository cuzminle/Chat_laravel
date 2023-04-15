<template>
    <div class = "w-1/2 mx-auto py-6">
        <div>
            <div class="mb-4">
                <input type = "text" v-model="body" class="rounded-full border border-gray-400" placeholder="your message">
            </div>
            <div class="mb-4">
                <a @click.prevent="store" href = "#" class="rounded-lg block w-48 bg-sky-400 text-white text-center py-2">Send</a>
            </div>
        </div>
        <div class="mb-4">
            <h3 class="text-center pb-4 mb-4">Messages</h3>
            <div class="text-sm pb-4 mb-4 border-b border-grey" v-for="message in messages">
                <p>{{message.id}}</p>
                <p>{{message.body}}</p>
                <p class="text-right">{{message.time}}</p>
            </div> 
        </div>
    </div>
    
</template>
<script>

export default {
    name: 'index',

    props: [
        'messages'
    ],

    data() {
        return {
            body: ''
        }
    },

    created() {
        window.Echo.channel('store-message')
        .listen('.store-message', res => {
            this.messages.unshift(res.message)
        })
    },

    methods: {
        store() {
            axios.post('/messages', {body: this.body})
            .then(res => {
                this.messages.unshift(res.data)
                this.body = ''
            })
           
        }
    }
}
</script>
<style lang="">
    
</style>