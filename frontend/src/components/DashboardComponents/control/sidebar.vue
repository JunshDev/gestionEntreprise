<template>
    <div >
        <div  class="sticky top-0 bg-dash-bleu h-screen overflow-hidden" :class=" isShow ? 'w-56   ': 'w-16   ' ">
            <div class="absolute top-20 right-2   rotate-90 bg-secondary rounded-full text-primary  text-5xl" :class="isShow? 'z-50 ':'-rotate-90  z-50'"   v-on:click="show">
                <i class="fa-solid fa-circle-chevron-down "></i>
                
                
            </div>
        <a href="/">
        <img src="../../../assets/images/logo.svg" :class=" isShow? ' p-12  pt-16 ' : 'pt-4 hidden'" alt="logo ">
        <img src="../../../assets/images/logo1.svg" :class=" isShow? '  hidden ' : 'pt-12 p-2 '" alt="logo ">
        </a>  
        <div class="menu-items flex flex-col " :class="isShow? 'mt-8': 'mt-[5rem]'">
            <!-- <router-link to ="/profile" class="side-btn " :active-class="isShow? 'active text-bg-bg-bleu' : 'active1'" tag="button"> <div :class="isShow ? 'link-container  pl-16':'pl-4 '"> <span class="pr-4"> <i class="fa-solid fa-user-helmet-safety"  style="color:#FFAA4C   !important;" ></i></span> <span v-if="isShow" class="" > Personnel  </span></div></router-link> -->
            <router-link to ="/statistic" class="side-btn " :active-class="isShow? 'active text-bg-bg-bleu' : 'active1'" tag="button"> <div :class="isShow ? 'link-container  pl-16':'pl-4 '"> <span class="pr-4"><i class="fa-solid fa-chart-line"  style="color:#FFAA4C   !important;"></i></span> <span v-if="isShow"  > statistic </span></div></router-link>
            <router-link to ="/orders" class="side-btn " :active-class="isShow? 'active text-bg-bg-bleu' : 'active1'" tag="button"> <div :class="isShow ? 'link-container  pl-16':'pl-4 '"> <span class="pr-4"><i class="fa-solid fa-chart-line"  style="color:#FFAA4C   !important;"></i></span>  <span v-if="isShow"  > Order </span></div></router-link>
            <router-link to ="/profile" class="side-btn " :active-class="isShow? 'active text-bg-bg-bleu' : 'active1'" tag="button"> <div :class="isShow ? 'link-container  pl-16':'pl-4 '"> <span class="pr-4"> <i class="fa-solid fa-person-digging"  style="color:#FFAA4C   !important;" ></i></span> <span v-if="isShow"  > Personnel  </span></div></router-link>
            <router-link to ="/customers" class="side-btn " :active-class="isShow? 'active text-bg-bg-bleu' : 'active1'" tag="button"> <div :class="isShow ? 'link-container  pl-16':'pl-4 '"> <span class="pr-4"><i class="fa-solid fa-chart-line"  style="color:#FFAA4C   !important;"></i></span>  <span v-if="isShow"  > Customer </span></div></router-link>
            <router-link to ="/product" class="side-btn " :active-class="isShow? 'active text-bg-bg-bleu' : 'active1'" tag="button"> <div :class="isShow ? 'link-container  pl-16':'pl-4 '"><span class="pr-4"> <i class="fa-solid fa-chart-line"  style="color:#FFAA4C   !important;"></i></span> <span v-if="isShow"  > Product </span></div></router-link>
            
            
        </div>
        </div>
    </div>
</template>
<script>
export default {
    props:{
        isShow:Boolean,
        show: Function,
    },

        }

</script>

<style scoped>

.menu-items {
    display: flex;
    flex-direction: column;
    /* margin-top: 40px; */
    margin-left: 6px;
}
.menu-items > * {
    margin-top: 40px;
}
.side-btn {
    border: none;
    padding: 16px 0px;
    cursor: pointer;
    font-size: 16px;
    font-weight: 500;
    color: #f9F9F9;
    background-color: transparent;
}
.side-btn:focus {
    outline: none;
}
.side-btn.active {
    position: relative;
    background-color: #f9F9F9;
    color :#001E6C;
    font-weight: 600;
    margin-left: 10px;
    border-radius: 30px 0 0 30px;
}
.side-btn.active::before {
    top: -30px;
}
.side-btn.active::after {
    bottom: -30px;
}
.side-btn.active::before, .side-btn.active::after {
    position: absolute;
    content: "";
    right: 0;
    height: 30px;
    width: 30px;
    background-color: #F9F9F9;
}
.side-btn.active1 {
    position: relative;
    background-color: #F9F9F9;
    color : #001E6C;
    font-weight: 600;
    
    border-radius: 30px 0 0 30px;
}
.side-btn.active1::before {
    top: -30px;
}
.side-btn.active1::after {
    bottom: -30px;
}
.side-btn.active1::before, .side-btn.active1::after {
    position: absolute;
    content: "";
    right: 0;
    height: 30px;
    width: 30px;
    
    background-color: #e7000000;
}



.side-btn.active .link-container::before {
    top: -60px;
}
.side-btn.active .link-container::after {
    bottom: -60px;
    z-index: 99;
}

.side-btn.active .link-container::before, .side-btn.active .link-container::after {
    position: absolute;
    content: "";
    right: 0px;
    height: 60px;
    width: 60px;
    border-radius: 50%;
    background-color: #001E6C;
}.side-btn.active .link-container::before {
    top: -60px;
}
.side-btn.active .link-container::after {
    bottom: -60px;
    z-index: 99;
}

.side-btn.active .link-container::before, .side-btn.active .link-container::after {
    position: absolute;
    content: "";
    right: 0px;
    height: 60px;
    width: 60px;
    border-radius: 50%;
    background-color: #001E6C;
}
</style>