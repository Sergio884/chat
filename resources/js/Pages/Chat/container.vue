<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Chat
            </h2>
        </template>

        <div class="contenedor-chat">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <messageContainer></messageContainer>
                    <InputMessage />
                </div>

            </div>
        </div>

    </AppLayout>
    <FooterLayout/>
</template>

<script>
import AppLayout from '@/Layouts/AppLayout.vue';
import FooterLayout from '@/Layouts/FooterLayout.vue';
import messageContainer from './messageContainer.vue';
import InputMessage from './inputMessage.vue';
import axios from 'axios';

export default {
    components: {
        AppLayout,
        FooterLayout,
        messageContainer,
        InputMessage
    },
    data: function(){
        return {
            chatRooms: [],
            currentRoom: "",
            messages:[]
        }
    },
    methods:{
        getRooms(){
            axios.get('/chat/rooms')
            .then( response => {
                this.chatRooms = response.data
                this.setRoom(response.data[0])
            })
        },
        setRoom(room){
            this.currentRoom = room
            console.log(this.currentRoom.name)
            this.getMessages(this.currentRoom.id)
        },
        getMessages(id){
            axios.get('/chat/room/'+id+'/messages')
            .then(response =>{
                this.messages = response.data
                console.log(this.messages)
            })
        }
    },
    created(){
        this.getRooms();
    }
}
</script>
<style>
.contenedor-chat{
    margin-top: 30px;
    background: red;
}
</style>
