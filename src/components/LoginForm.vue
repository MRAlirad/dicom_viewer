<template>
    <div class="loginWays flex gap-[100px] relative">
                <button 
                    id="button"
                    class="button text-[#4e51fe] text-[15px] tracking-wide font-bold hover:text-blue-700">By Username</button>
                <button class="text-[#4e51fe] text-[15px] tracking-wide font-bold hover:text-blue-700">By SMS</button>
                <div id="active" class="active before:content-[' '] w-[101px] h-[2px] bg-[#91B3FA] absolute left-[-2px] bottom-[-4px]"></div>
            </div>
    <div class="form p-[45px] w-[87%]">
        <form class="formE1 w-[98%] flex flex-col gap-[50px]">
            <div class="inputs flex flex-col gap-10" v-if="activeInput === 'username'" >
                <input 
                    type="text"
                    placeholder="Enter Your Username"
                    v-model="username.value" 
                    @click="userActive" 
                    class="text-[#1e1b4b] w-full border-b-2 border-b-[#91B3FA] placeholder-[#A18F8F] placeholder-opacity-100 placeholder-[20px] placeholder-font-medium bg-[#e9f0ff] focus:outline-none" >
            <input 
                type="password" 
                placeholder="Enter Your password" 
                v-model="password.value"
                @click="passActive" 
                class="w-full text-[#1e1b4b] border-b-2 border-b-[#91B3FA] placeholder-[#A18F8F] placeholder-opacity-100 placeholder-[12px] placeholder-font-medium bg-[#e9f0ff] focus:outline-none invalid:text-pink-600" >
            </div>
            <div class="forget-remember flex justify-between gap-[10px] mt-[-43px]">
                <label for="remember" class="remember flex gap-0.5 text-[13px] text-[#7f7070] font-normal cursor-pointer"><input type="checkbox" id="remember"  class="remember">Remember me</label>
                <a href="#" class="forget text-[13px] text-[#4E51FE] font-medium hover:text-blue-700">Forget Password?</a>
            </div>
            <button class="login mt-[30px] bg-[#7D97F4] text-[#fff] border-2 border-solid border-[#7D97F4] rounded-md font-bold text-[15px] w-max pt-[10px] pb-[10px] pr-[30px] pl-[30px] m-auto hover:bg-blue-500 hover:border-blue-500">LOGIN</button>
        </form>
    </div>
</template>

<script>
export default {
    data(){
        return{
            activeInput : 'username',
            username : {
                value : ''
            },
            password : {
                value : ''
            }
        }
    },

    method : {
        userActive(){
            this.activeInput === 'username'
        },
        passActive(){
            this.activeInput === 'password'
        }
    }
}
</script>

<style>

</style>