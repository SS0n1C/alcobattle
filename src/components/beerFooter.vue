<template>
  <footer class="footer">
    <div class="footerField">
        <div class="footerField__logo">
            <div class="footerField__logo--place">
                <img src="../assets/img/logo.png" alt="logo">
            </div>
        </div>
        <div class="footerField__info">
            <div class="footerField__info--txt">
                © 2010-2023
            </div>
        </div>
        <div class="footerField__social">
            <div class="footerField__social--item" v-for="(social,i) in getAllSocial" :key="i">
                <a :href="social.link" rel="noopener noreferrer">
                    <!-- <svg>
                        <use xlink:href='../assets/img/sprite.svg#search'></use>  
                    </svg> -->
                    <svg>
                        <use :xlink:href=social.icon></use>
                    </svg>
                </a>
            </div>
        </div>
    </div>
  </footer>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
    data(){
        return {
            
        }
    },
computed:{
    ...mapGetters(["getAllSocial"])

},
methods:{

}
}
</script>

<style>

</style>