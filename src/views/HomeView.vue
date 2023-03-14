<template>
    <div class="home">
        <p>this is home page</p>
        <VueRecaptcha
            :sitekey="siteKey"
            :load-recaptcha-script="true"
            @verify="handleSuccess"
            @error="handleError"
        ></VueRecaptcha>
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import { VueRecaptcha } from 'vue-recaptcha'

export default {
    name: 'HomeView',
    
    components: {
        HelloWorld,
        VueRecaptcha
    },
    data(){
        return{
            siteKey:'6LfmLPgkAAAAAGtijq-COsEqioPSu2Vvh3SiLyeS'
        }
    },
    methods:{
        handleSuccess(){
            console.log('ok')
        },
        handleError(){
            console.log('cancel')
        }
    }
    
}
</script>
