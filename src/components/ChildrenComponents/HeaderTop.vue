<template>
    <div class="header__top" v-show="show">
        <div class="container">
            <div class="col-3 col-sm-3">
                <router-link class="header__logo" to="/" >
                    <!-- :style="{ backgroundImage: url('../../assets/images/logo.svg') }" -->
                    <!-- <img class="header__logo" src="../../assets/images/logo.svg" alt="logo"> -->
                    <svg v-if="logo" class="header__logo" width="184" height="60" viewBox="0 0 184 60" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <rect width="184" height="60" fill="white"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M165.443 31.2233H171.59L177.345 42.7573H173.156L172.06 40.8155H164.934L163.838 42.7573H159.649L165.443 31.2233ZM135.416 33.9417V34.7961V39.9223V42.7573H139.018V39.9223V32.4272V31.2233H133.146L126.999 39.767C126.96 39.8835 126.921 39.9612 126.843 40.0777V39.1845V35.068V31.2233H123.241V35.068V41.9029V42.7573H129.113L135.26 34.2136C135.338 34.1359 135.377 34.0194 135.416 33.9417ZM168.81 33.8252H168.262L166.305 37.8252H170.729L168.81 33.8252ZM143.05 31.2233H146.652V35.2621H148.531L152.603 31.2233H157.535L151.702 36.7379L158.279 42.7961H153.072L148.531 38.2913H146.652V42.7961H143.05V31.2233ZM104.997 31.2233H108.599V35.2621H116.351V31.2233H119.952V42.7573H116.351V38.2524H108.599V42.7573H104.997V31.2233ZM86.8715 31.1845L92.1957 36.8544L86.8715 42.7573H91.6868L95.2102 38.8738L98.7336 42.7573H103.549L98.2247 36.8544L103.549 31.1845H98.577L95.2102 34.9126L91.8434 31.1845H86.8715ZM72.3864 42.7573V31.1845H84.9532V33.9806H75.9881V35.6116H84.5617V38.4078H75.9881V40H84.9532V42.7961H72.3864V42.7573ZM56.3745 34.1748V31.1845H70.2332V34.1748H65.1047V42.7573H61.503V34.1748H56.3745Z" fill="#2A5275"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M156.674 14.0583V9.5534H177.384V14.0194H169.711V26.835H164.347V14.0194H156.674V14.0583ZM78.2587 9.63107V26.9126H83.6221V14.7961L90.6689 26.9126H95.0536L101.631 14.7961V26.9126H106.329L108.403 19.4563L106.603 19.4175L108.677 9.63107H97.8723L93.2919 19.301H92.4698L87.8894 9.63107H78.2587V9.63107ZM66.5923 22.9903C69.1762 22.9903 70.6638 22.9515 71.0553 22.8738C71.4468 22.7961 71.6817 22.4854 71.6817 21.9417C71.6817 21.2816 71.4077 20.8544 70.8204 20.699C70.2332 20.5437 68.8238 20.4272 66.5923 20.4272C62.1294 20.4272 59.3106 20.1165 58.1362 19.4563C56.9617 18.7961 56.3745 17.2039 56.3745 14.6796C56.3745 12.3107 57.1183 10.835 58.6451 10.1748C59.8196 9.6699 62.4034 9.43689 66.4357 9.43689C70.0374 9.43689 72.3081 9.51456 73.2477 9.70874C75.0485 10.0583 76.1447 11.3398 76.497 13.5922H66.5532H66.4357C64.0085 13.5922 62.6383 13.6311 62.2468 13.7087C61.8553 13.7864 61.6987 14.1359 61.6987 14.6796C61.6987 15.2621 62.0119 15.6505 62.6383 15.8447C63.2647 16.0388 64.5566 16.1165 66.5532 16.1165C70.977 16.1165 73.7957 16.466 75.0877 17.165C76.3796 17.8641 77.006 19.4563 77.006 21.9417C77.006 24.233 76.3013 25.7087 74.8528 26.3689C73.6 26.9126 70.8596 27.1845 66.514 27.1845C63.1864 27.1845 61.0332 27.1068 60.0545 26.9515C58.5277 26.7184 57.4706 26.2136 56.9225 25.3592C56.5702 24.8155 56.3353 24.0388 56.1787 22.9903H66.3966H66.5923V22.9903ZM115.568 9.63107H124.963L133.576 26.8738H127.312L125.668 23.9612H115.059L113.414 26.8738H107.151L107.19 26.7961L114.315 16.9709L111.066 16.7767L115.568 9.63107ZM120.735 13.5146H119.913L117.016 19.4951H123.632L120.735 13.5146ZM134.281 9.5534H149.862C151.78 9.5534 153.151 9.90291 153.934 10.6019C154.795 11.3398 155.226 12.699 155.226 14.6019C155.226 16.0777 155.03 17.2039 154.677 17.9029C154.325 18.6019 153.699 19.1456 152.798 19.4951C153.777 19.9223 154.403 20.3495 154.717 20.7379C155.03 21.165 155.186 21.9029 155.186 22.9903V26.8738H149.823V23.767C149.823 23.301 149.706 22.9515 149.471 22.6408C149.157 22.2524 148.688 22.0194 148.1 22.0194H139.644V26.835H134.281V9.5534ZM139.605 14.0583V17.5922H148.218C148.805 17.5922 149.236 17.4757 149.471 17.2039C149.706 16.9709 149.862 16.5049 149.862 15.8447C149.862 15.1845 149.745 14.7184 149.471 14.4466C149.197 14.1748 148.805 14.0583 148.218 14.0583H139.605Z" fill="#4878A6"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M10.1396 13.3592L16.9515 9.47573L26.1906 4.19417L35.4298 9.47573L44.6689 14.7573V20.8932L39.3055 17.8252L26.1906 10.2913L15.503 16.4272L10.1396 13.3592ZM7.71234 17.5146V23.8058L26.5038 34.5631L31.7498 31.2621L7.71234 17.5146Z" fill="#4878A6"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M42.2417 37.2816L35.4298 41.165L26.1906 46.4466L16.9515 41.165L7.71234 35.8835V29.7476L13.0757 32.8155L26.1906 40.3107L36.8783 34.1748L42.2417 37.2816ZM30.6928 18.7961L26.3081 16.2719L21.1404 19.2233L24.4289 21.1262L43.2204 31.8835L44.7081 32.7379V26.7961L43.2204 25.9418L30.6928 18.7961Z" fill="#2A5275"/>
                    </svg>
                    <svg v-else class="header__logo" width="184" height="60" viewBox="0 0 184 60" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <rect width="184" height="60" fill="#EDF2F6"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M165.443 31.2233H171.59L177.345 42.7573H173.156L172.06 40.8155H164.934L163.838 42.7573H159.649L165.443 31.2233ZM135.416 33.9417V34.7961V39.9223V42.7573H139.018V39.9223V32.4272V31.2233H133.146L126.999 39.767C126.96 39.8835 126.921 39.9612 126.843 40.0777V39.1845V35.068V31.2233H123.241V35.068V41.9029V42.7573H129.113L135.26 34.2136C135.338 34.1359 135.377 34.0194 135.416 33.9417ZM168.81 33.8252H168.262L166.305 37.8252H170.729L168.81 33.8252ZM143.05 31.2233H146.652V35.2621H148.531L152.603 31.2233H157.535L151.702 36.7379L158.279 42.7961H153.072L148.531 38.2913H146.652V42.7961H143.05V31.2233ZM104.997 31.2233H108.599V35.2621H116.351V31.2233H119.952V42.7573H116.351V38.2524H108.599V42.7573H104.997V31.2233ZM86.8715 31.1845L92.1957 36.8544L86.8715 42.7573H91.6868L95.2102 38.8738L98.7336 42.7573H103.549L98.2247 36.8544L103.549 31.1845H98.577L95.2102 34.9126L91.8434 31.1845H86.8715ZM72.3864 42.7573V31.1845H84.9532V33.9806H75.9881V35.6116H84.5617V38.4078H75.9881V40H84.9532V42.7961H72.3864V42.7573ZM56.3745 34.1748V31.1845H70.2332V34.1748H65.1047V42.7573H61.503V34.1748H56.3745Z" fill="#2A5275"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M156.674 14.0583V9.5534H177.384V14.0194H169.711V26.835H164.347V14.0194H156.674V14.0583ZM78.2587 9.63107V26.9126H83.6221V14.7961L90.6689 26.9126H95.0536L101.631 14.7961V26.9126H106.329L108.403 19.4563L106.603 19.4175L108.677 9.63107H97.8723L93.2919 19.301H92.4698L87.8894 9.63107H78.2587V9.63107ZM66.5923 22.9903C69.1762 22.9903 70.6638 22.9515 71.0553 22.8738C71.4468 22.7961 71.6817 22.4854 71.6817 21.9417C71.6817 21.2816 71.4077 20.8544 70.8204 20.699C70.2332 20.5437 68.8238 20.4272 66.5923 20.4272C62.1294 20.4272 59.3106 20.1165 58.1362 19.4563C56.9617 18.7961 56.3745 17.2039 56.3745 14.6796C56.3745 12.3107 57.1183 10.835 58.6451 10.1748C59.8196 9.6699 62.4034 9.43689 66.4357 9.43689C70.0374 9.43689 72.3081 9.51456 73.2477 9.70874C75.0485 10.0583 76.1447 11.3398 76.497 13.5922H66.5532H66.4357C64.0085 13.5922 62.6383 13.6311 62.2468 13.7087C61.8553 13.7864 61.6987 14.1359 61.6987 14.6796C61.6987 15.2621 62.0119 15.6505 62.6383 15.8447C63.2647 16.0388 64.5566 16.1165 66.5532 16.1165C70.977 16.1165 73.7957 16.466 75.0877 17.165C76.3796 17.8641 77.006 19.4563 77.006 21.9417C77.006 24.233 76.3013 25.7087 74.8528 26.3689C73.6 26.9126 70.8596 27.1845 66.514 27.1845C63.1864 27.1845 61.0332 27.1068 60.0545 26.9515C58.5277 26.7184 57.4706 26.2136 56.9225 25.3592C56.5702 24.8155 56.3353 24.0388 56.1787 22.9903H66.3966H66.5923V22.9903ZM115.568 9.63107H124.963L133.576 26.8738H127.312L125.668 23.9612H115.059L113.414 26.8738H107.151L107.19 26.7961L114.315 16.9709L111.066 16.7767L115.568 9.63107ZM120.735 13.5146H119.913L117.016 19.4951H123.632L120.735 13.5146ZM134.281 9.5534H149.862C151.78 9.5534 153.151 9.90291 153.934 10.6019C154.795 11.3398 155.226 12.699 155.226 14.6019C155.226 16.0777 155.03 17.2039 154.677 17.9029C154.325 18.6019 153.699 19.1456 152.798 19.4951C153.777 19.9223 154.403 20.3495 154.717 20.7379C155.03 21.165 155.186 21.9029 155.186 22.9903V26.8738H149.823V23.767C149.823 23.301 149.706 22.9515 149.471 22.6408C149.157 22.2524 148.688 22.0194 148.1 22.0194H139.644V26.835H134.281V9.5534ZM139.605 14.0583V17.5922H148.218C148.805 17.5922 149.236 17.4757 149.471 17.2039C149.706 16.9709 149.862 16.5049 149.862 15.8447C149.862 15.1845 149.745 14.7184 149.471 14.4466C149.197 14.1748 148.805 14.0583 148.218 14.0583H139.605Z" fill="#4878A6"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M10.1396 13.3592L16.9515 9.47573L26.1906 4.19417L35.4298 9.47573L44.6689 14.7573V20.8932L39.3055 17.8252L26.1906 10.2913L15.503 16.4272L10.1396 13.3592ZM7.71234 17.5146V23.8058L26.5038 34.5631L31.7498 31.2621L7.71234 17.5146Z" fill="#4878A6"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M42.2417 37.2816L35.4298 41.165L26.1906 46.4466L16.9515 41.165L7.71234 35.8835V29.7476L13.0757 32.8155L26.1906 40.3107L36.8783 34.1748L42.2417 37.2816ZM30.6928 18.7961L26.3081 16.2719L21.1404 19.2233L24.4289 21.1262L43.2204 31.8835L44.7081 32.7379V26.7961L43.2204 25.9418L30.6928 18.7961Z" fill="#2A5275"/>
                    </svg>
                    <!-- <img src="../../assets/images/logoBlueBackground.svg" alt=""> -->
                </router-link>
            </div>
            <div :class="['header__info', 'col-6']">
                <div class="header__contacts" >
                    <a href="tel:+7 (958) 111-95-03">+7 (958) 111-95-03</a>
                    <a href="tel:+7 (958) 111-95-03">+7 (958) 111-95-03</a>
                </div>
                <div :class="['header__job--search']">
                    <p  class="header__jobtime">Пн-вс: с 10:00 до 21:00</p>
                </div>
                <div :class="['header__searchbox']">
                    <button>
                        <img src="../../assets/images/search.svg" alt="search">
                    </button>
                    <input @click.left="search" :class="['header__search']" type="text" placeholder="Поиск...">
                </div>
            </div>
            <div class="header__right col-3 col-sm-9">
                <div class="header__btns">
                    <router-link to="/">
                        <img class="header__btn" src="../../assets/images/eye.svg" alt="eye">
                    </router-link>
                    <router-link to="/favorites">
                        <img class="header__btn" src="../../assets/images/heart.svg" alt="heart">
                    </router-link>
                    <router-link to="/">
                        <img class="header__btn" src="../../assets/images/compair.svg" alt="compair">
                    </router-link>
                    <router-link to="/">
                        <img class="header__btn" src="../../assets/images/basketHeader.svg" alt="basket">
                    </router-link>
                </div>
                <button v-if="check" @click="$store.dispatch('setAuthToggle', true)" class="header__signup">
                    Войти
                </button>
                <router-link v-else class="header__profile"  to="/account">
                    <img src="../../assets/images/profile-img.svg" alt="">
                </router-link>
            </div>
        </div>
    </div>
    <div class="header__top--other" v-show="showBig">
        <div class="container">
            <search-box></search-box>
            <!-- <div class="header__bigSearchbox col-11">
                <input class="header__bigSearch" type="text" placeholder="Введите запрос, например «Smart balance»">
            </div> -->
            <div class="header__right--btn ">
                <button class="header__close--btn" @click="close">
                    <img class="header__close--img" src="../../assets/images/closeBtn.svg" alt="">
                </button>
            </div>
        </div>
    </div>
</template>

<script>
import axios from "axios";
import SearchBox from '@/components/SearchBox'

export default {
    data() {
        return {
            show : true,
            isActive : false,
            logo : true
            // check : false
        }
    },
    methods: {
        search(){
            this.show = false
            this.$store.dispatch('setClose', true)
        },
        close(){
            this.show = true
            this.$store.dispatch('setClose', false)
        },
    },
    computed : {
        showBig(){
            return this.$store.getters.close;
        },
        check(){
            return this.$store.getters.getCheck
        },
    },
    watch: {
        $route(newValue){
            if(newValue.path !== '/') {
                this.show = true
                this.$store.dispatch('setClose', false)
            }
        }
    },
    setup(){
        // const show = ref(true)
        // const isActive = ref(false)
        // const store = useStore()
        // const navigation = useRoute()
        
        // const framework = reactive({
        //     show : true,
        //     isActive : false
        // })

        // function search() {
        //     show.value = false
        //     store.dispatch('setClose', true)
        // }

        // function close(){
        //     show.value = true
        //     store.dispatch('setClose', false)
        // }

        // const showBig = computed(() => store.getters.close)
        // let check = computed(() => store.getters.getCheck)

        // watch(showBig, (newValue, oldValue) => {
        //     console.log(newValue, oldValue);
        // })

        
        // watch(navigation, (newValue) => {
        //     if(newValue.path !== '/') {
        //         show.value = true
        //         store.dispatch('setClose', false)
        //     }
        // })

        // return {
        //     show, isActive, framework, search, showBig, close, check
        // }
    },
    components : {
        SearchBox
    },
    created(){
        window.addEventListener("scroll", () => {
            if (window.scrollY > 173) {
                document.querySelector(".header__top").classList.add("mini");
                this.logo = false
            } else {
                this.logo = true
                document.querySelector(".header__top").classList.remove("mini");
            }
        });
    },
    async beforeCreate(){
        
        if(this.$cookies.isKey('eltechusers')) {
            let userID = this.$cookies.get('eltechusers')
            console.log(userID);
            const {data} =  await axios.get('https://vue-eltech-userinfo-default-rtdb.firebaseio.com/users.json')
            let result = Object.keys(data).map(key => {
                return {
                    id : key,
                    ...data[key]
                }
            })
            let arrID = []
            result.forEach(res => {
                arrID.push(res.id)
            })
            if(arrID.includes(userID.slice(1,userID.length - 1))) {
                console.log('salom');
                this.$store.dispatch('setCheck', false) 
            } else {
                this.$store.dispatch('setCheck', true)
                console.log('xayr');
            }
            
        } else {
            this.$store.dispatch('setCheck', true)
            console.log('xayr');
        }  
    },
    
}
</script>

<style lang="sass" scoped>
    @import '../../styles/Components/TheHeader'
</style>