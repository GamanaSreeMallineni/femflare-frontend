<template>
    <div as="nav" class="fixed w-screen z-10 mt-16 ">
        <div class="flex items-center">
            <div>
                <img class="h-5 w-auto ml-5 lg:h-10 inline" src="../assets/kl_logo.png" alt="Logo" />
                <img class="h-5 w-auto mx-5 lg:h-10 inline" src="../assets/klh.png" alt="Logo" />
            </div>
            <img class="h-20 w-auto ml-auto mr-10 mt-2 mx-4 lg:h-20" src="../assets/womens_logo.png" alt="Logo" />
        </div>
    </div>
    <div class="background  " style="z-index: 0;">
        <span v-for="i in 100">
        </span>

    </div>


    <kinesis-container>
        <div class="bg-transparent min-h-screen flex items-center justify-center">
            <div class="container mx-auto px-4">
                <div class="flex flex-col items-center justify-center text-center" v-if="isLargeScreen">
                    <kinesis-element :strength="10">
                        <h1 class="mt-20 text-5xl lg:text-9xl font-extrabold text-transparent bg-gradient-to-r from-green-800 via-blue-800 to-purple-800 bg-clip-text mb-8 "
                            style="font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;">
                            FEMFLARE 2025</h1>
                    </kinesis-element>
                    <div class="flex items-center justify-center mb-8">

                        <div class="flex flex-col items-center">
                            <kinesis-element :strength="5">
                                <Countdown labelColor="black" deadlineISO="2025-03-21 00:00:00" mainColor="#FF407D" />
                            </kinesis-element>
                        </div>
                    </div>
                    <p class="text-lg text-gray-900 mb-8">Join us for the most amazing event of the year!</p>
                    <RouterLink to="signup" class="button text-green-900 border-stone-900" v-if="!authStore.isAuth">
                        Register Here!
                    </RouterLink>
                </div>
                <div class="flex flex-col items-center justify-center text-center" v-else>

                    <h1 class="mt-15 text-5xl font-bold text-pink-500 mb-8 "
                        style="font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;">
                        FEMFLARE 2025</h1>


                    <div class="flex items-center justify-center mb-8">

                        <div class="flex flex-col items-center">


                            <Countdown labelColor="#ffffff" deadlineISO="2025-03-21 00:00:00" mainColor="#FF407D" />

                        </div>
                    </div>
                    <p class="text-lg text-gray-900 mb-8">Join us for the most amazing event of the year!</p>

                    <RouterLink to="signup" class="button text-green-900 border-stone-900" v-if="!authStore.isAuth">
                        Register Here!
                    </RouterLink>


                </div>
            </div>
        </div>
    </kinesis-container>

    <section class="bg-gray-900 absolute w-full z-10" id="about">

        <div class="  grid max-w-screen-xl px-4 py-8 mx-auto lg:gap-8 xl:gap-0 lg:py-16 lg:grid-cols-12">
            <div class="mobile-only mb-12 lg:mt-0 lg:col-span-6 lg:flex ">
                <img src="../assets/logo.png" alt="mockup" class="animate-pulse">
            </div>
            <div class="mr-auto place-self-center lg:col-span-6">
                <h1 class="max-w-2xl mb-4 text-3xl font-extrabold tracking-tight leading-none md:text-4xl xl:text-5xl text-gray-50"
                    style="font-family: 'Tangerine', serif; color: rgb(246, 51, 165);">Celebration of
                    Womenhood</h1>
                <p
                    class="max-w-2xl mb-6 font-light text-gray-50 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-50 text-justify">
                    FemFlare is more than just a festival, it’s a movement! Under this year’s theme, 
                    <b>AccelerateAction</b>, we bring together diverse women from across the globe to drive change, 
                    showcase talents, and build lasting connections. This two-day extravaganza is designed to 
                    empower women through dynamic workshops, thought-provoking talks, and inspiring exhibitions, 
                    fostering leadership and innovation. Hear success stories of trailblazing women who have 
                    shattered barriers and turned aspirations into reality. Engage with experts in business, 
                    technology, arts, and social justice, and stand a chance to win ₹1 lakh in prize money. 
                    Join us as we take bold steps toward a more inclusive and equitable future - because together,
                     we don’t just dream of change, we AccelerateAction! </p>
            </div>
            <div class="desktop-only lg:mt-0 lg:col-span-6 lg:flex ">
                <img src="../assets/logo.png" alt="mockup" class="animate-pulse">
            </div>
        </div>

        <div class="grid max-w-screen-xl px-4 py-8 mx-auto lg:gap-8 xl:gap-0 lg:py-16 lg:grid-cols-12">
            <div class="mx-auto place-self-center  lg:col-span-5">

                <img src="../assets/kl_logo.png" alt="image" />

            </div>
            <div class="mr-auto place-self-center lg:col-span-7">

                <p
                    class="ml-12 max-w-2xl mb-6 font-light text-gray-50 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-50 text-justify">
                    K L University shines in the prestigious NIRF 2023 Rankings, securing impressive positions across
                    multiple categories. Ranked #28 in Universities, #44 in Engineering, #52 in Management, and #50
                    Overall, this accomplishment highlights our dedication to academic excellence and holistic
                    development</p>
            </div>

        </div>
        <div class="container grid max-w-screen-xl px-4 py-8 mx-auto lg:gap-8 xl:gap-0 lg:py-16 lg:grid-cols-12">
            
            <div class="mobile-only mx-auto place-self-center lg:col-span-6">

                <img src="../assets/womens_logo.png" alt="image" class="w-64 h-64 md:h-80 md:w-80" />

            </div>
            <div class=" lg:mt-0 lg:col-span-6 lg:flex">

                <p
                    class="max-w-2xl mb-6 font-light text-gray-50 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-50 text-justify">
                    The Women Development Cell (WDC) at KLEF promotes gender equality through education, advocacy, and
                    skill-building initiatives. Our mission includes creating a safe environment for women to thrive,
                    offering awareness programs on women's rights, and conducting gender sensitization activities on
                    campus. We strive to address gender discrimination, prevent sexual harassment, and ensure equitable
                    opportunities for all genders within the university community.</p>
            </div>
            <div class="desktop-only mx-auto place-self-center lg:col-span-6">

                <img src="../assets/womens_logo.png" alt="image" class="w-64 h-64 md:h-80 md:w-80" />

            </div>


        </div>
        
        <!-- <div class="  grid max-w-screen-xl space-x-5 px-4 py-8 mx-auto lg:gap-8 xl:gap-0 lg:py-16 lg:grid-cols-12">

            <div class="lg:mt-0 lg:col-span-5 lg:flex">
                <img class="rounded-xl" src="../assets/djreha.png">
            </div>
            <div class="mr-auto place-self-center lg:col-span-7">

                <p
                    class="max-w-2xl mb-6 font-light text-gray-50 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-50 text-justify">
                    DJ Rhea, is a powerhouse in the world of DJs, Seamlessly blending genres and captivating audiences
                    worldwide, she's a force in the industry. Whether at sold-out festivals or prestigious clubs, her
                    distinctive style and unique beats leave a lasting impression. With 655k followers on Instagram, DJ
                    Rhea's magnetic charisma continues to draw fans from every corner of the country, solidifying her as
                    one of the most exciting talents in the field.</p>
            </div>
        </div> -->
        <div class="h-full w-full bg-gray-50">
            <img src="../assets/KL_Ranks.jpg" alt="image" class="w-full h-30" />
        </div>
    </section>

</template>

<script setup>

import { ref, onMounted, onUnmounted } from 'vue';
import { KinesisContainer, KinesisElement } from 'vue-kinesis'
import { Countdown } from 'vue3-flip-countdown'
import { useAuthStore } from '../stores/auth.js'
import { RouterLink } from 'vue-router';

const authStore = useAuthStore()
const isLargeScreen = ref(window.matchMedia('(min-width: 768px)').matches);
console.log(isLargeScreen)
const handleResize = () => {
    isLargeScreen.value = window.matchMedia('(min-width: 768px)').matches;
};

onMounted(() => {
    window.addEventListener('resize', handleResize);
});

onUnmounted(() => {
    window.removeEventListener('resize', handleResize);
});
</script>

<style scoped>
.button {
    position: relative;
    width: 140px;
    height: 40px;
    display: flex;
    align-items: center;
    color: black;
    background-color: #FFACAC;
    flex-direction: column;
    justify-content: center;
    border: none;
    padding: 12px;
    gap: 12px;
    border-radius: 8px;
    border-color: black;
    border-width: 10px;
    cursor: pointer;
}

.button::before {
    content: '';
    position: absolute;
    inset: 0;
    left: -4px;
    top: -1px;
    margin: auto;
    width: 148px;
    height: 48px;
    border-radius: 10px;
    background: linear-gradient(-45deg, #e81cff 0%, #40c9ff 100%);
    z-index: -10;
    pointer-events: none;
    transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

/* Default: Hide mobile image and show desktop image */
.mobile-only {
  display: none;
}

/* Show mobile image, hide desktop image on small screens */
@media (max-width: 768px) {
  .mobile-only {
    display: block;
  }
  .desktop-only {
    display: none;
  }
}

.button::after {
    content: "";
    z-index: -1;
    position: absolute;
    inset: 0;
    background: linear-gradient(-45deg, #fc00ff 0%, #00dbde 100%);
    transform: translate3d(0, 0, 0) scale(0.95);
    filter: blur(20px);
}

.button:hover::after {
    filter: blur(30px);
}

.button:hover::before {
    transform: rotate(-180deg);
}

.button:active::before {
    scale: 0.7;
}



@keyframes move {
    100% {
        transform: translate3d(0, 0, 1px) rotate(360deg);
    }
}

.background {
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
    background: pink;
    overflow: hidden;
}

.background span {
    width: 1vmin;
    height: 1vmin;
    border-radius: 1vmin;
    backface-visibility: hidden;
    position: absolute;
    animation: move;
    animation-duration: 6;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
}


.background span:nth-child(0) {
    color: #583C87;
    top: 73%;
    left: 89%;
    animation-duration: 182s;
    animation-delay: -210s;
    transform-origin: 13vw 4vh;
    box-shadow: -2vmin 0 0.5862519122595957vmin currentColor;
}

.background span:nth-child(1) {
    color: #FFACAC;
    top: 50%;
    left: 34%;
    animation-duration: 174s;
    animation-delay: -360s;
    transform-origin: -21vw -22vh;
    box-shadow: -2vmin 0 0.7042692211712167vmin currentColor;
}

.background span:nth-child(2) {
    color: #583C87;
    top: 84%;
    left: 54%;
    animation-duration: 351s;
    animation-delay: -268s;
    transform-origin: -21vw 4vh;
    box-shadow: 2vmin 0 0.9458767405205268vmin currentColor;
}

.background span:nth-child(3) {
    color: #E45A84;
    top: 36%;
    left: 54%;
    animation-duration: 217s;
    animation-delay: -233s;
    transform-origin: 8vw 13vh;
    box-shadow: 2vmin 0 0.6164698935915867vmin currentColor;
}

.background span:nth-child(4) {
    color: #E45A84;
    top: 9%;
    left: 16%;
    animation-duration: 426s;
    animation-delay: -413s;
    transform-origin: 10vw 8vh;
    box-shadow: -2vmin 0 1.051685910765597vmin currentColor;
}

.background span:nth-child(5) {
    color: #583C87;
    top: 5%;
    left: 86%;
    animation-duration: 354s;
    animation-delay: -5s;
    transform-origin: -6vw 19vh;
    box-shadow: 2vmin 0 0.25420719456850316vmin currentColor;
}

.background span:nth-child(6) {
    color: #FFACAC;
    top: 24%;
    left: 66%;
    animation-duration: 375s;
    animation-delay: -98s;
    transform-origin: -2vw 10vh;
    box-shadow: 2vmin 0 0.6675537448822226vmin currentColor;
}

.background span:nth-child(7) {
    color: #583C87;
    top: 28%;
    left: 35%;
    animation-duration: 334s;
    animation-delay: -217s;
    transform-origin: -18vw 11vh;
    box-shadow: -2vmin 0 0.5284886153891355vmin currentColor;
}

.background span:nth-child(8) {
    color: #FFACAC;
    top: 94%;
    left: 59%;
    animation-duration: 71s;
    animation-delay: -305s;
    transform-origin: 22vw -4vh;
    box-shadow: 2vmin 0 0.679744111971551vmin currentColor;
}

.background span:nth-child(9) {
    color: #583C87;
    top: 32%;
    left: 36%;
    animation-duration: 29s;
    animation-delay: -233s;
    transform-origin: -9vw 21vh;
    box-shadow: 2vmin 0 0.8466768492759915vmin currentColor;
}

.background span:nth-child(10) {
    color: #FFACAC;
    top: 81%;
    left: 35%;
    animation-duration: 171s;
    animation-delay: -382s;
    transform-origin: 18vw 3vh;
    box-shadow: 2vmin 0 1.1906330192616614vmin currentColor;
}

.background span:nth-child(11) {
    color: #583C87;
    top: 57%;
    left: 53%;
    animation-duration: 8s;
    animation-delay: -28s;
    transform-origin: 12vw -14vh;
    box-shadow: -2vmin 0 0.5025332909340516vmin currentColor;
}

.background span:nth-child(12) {
    color: #FFACAC;
    top: 39%;
    left: 4%;
    animation-duration: 433s;
    animation-delay: -106s;
    transform-origin: 21vw -12vh;
    box-shadow: -2vmin 0 0.5405247077993502vmin currentColor;
}

.background span:nth-child(13) {
    color: #FFACAC;
    top: 41%;
    left: 67%;
    animation-duration: 159s;
    animation-delay: -231s;
    transform-origin: 13vw 15vh;
    box-shadow: -2vmin 0 0.7788815428873603vmin currentColor;
}

.background span:nth-child(14) {
    color: #583C87;
    top: 6%;
    left: 78%;
    animation-duration: 209s;
    animation-delay: -279s;
    transform-origin: -21vw 17vh;
    box-shadow: 2vmin 0 0.6390630784750788vmin currentColor;
}

.background span:nth-child(15) {
    color: #E45A84;
    top: 90%;
    left: 26%;
    animation-duration: 276s;
    animation-delay: -300s;
    transform-origin: 17vw -6vh;
    box-shadow: 2vmin 0 0.7661324803526062vmin currentColor;
}

.background span:nth-child(16) {
    color: #E45A84;
    top: 67%;
    left: 34%;
    animation-duration: 133s;
    animation-delay: -111s;
    transform-origin: -2vw -11vh;
    box-shadow: 2vmin 0 0.5821850751260214vmin currentColor;
}

.background span:nth-child(17) {
    color: #583C87;
    top: 70%;
    left: 37%;
    animation-duration: 336s;
    animation-delay: -13s;
    transform-origin: -8vw 24vh;
    box-shadow: -2vmin 0 0.6200802316984944vmin currentColor;
}

.background span:nth-child(18) {
    color: #FFACAC;
    top: 67%;
    left: 55%;
    animation-duration: 191s;
    animation-delay: -342s;
    transform-origin: 20vw -21vh;
    box-shadow: -2vmin 0 0.8260502071680635vmin currentColor;
}

.background span:nth-child(19) {
    color: #583C87;
    top: 1%;
    left: 28%;
    animation-duration: 387s;
    animation-delay: -214s;
    transform-origin: 20vw -9vh;
    box-shadow: 2vmin 0 1.0759188507688522vmin currentColor;
}

.background span:nth-child(20) {
    color: #FFACAC;
    top: 65%;
    left: 5%;
    animation-duration: 437s;
    animation-delay: -157s;
    transform-origin: -18vw 7vh;
    box-shadow: -2vmin 0 1.021569667048151vmin currentColor;
}

.background span:nth-child(21) {
    color: #FFACAC;
    top: 49%;
    left: 3%;
    animation-duration: 319s;
    animation-delay: -309s;
    transform-origin: -15vw -2vh;
    box-shadow: -2vmin 0 0.9854816054279136vmin currentColor;
}

.background span:nth-child(22) {
    color: #E45A84;
    top: 24%;
    left: 94%;
    animation-duration: 326s;
    animation-delay: -20s;
    transform-origin: -20vw -17vh;
    box-shadow: 2vmin 0 0.5441809249091463vmin currentColor;
}

.background span:nth-child(23) {
    color: #583C87;
    top: 7%;
    left: 18%;
    animation-duration: 327s;
    animation-delay: -364s;
    transform-origin: -6vw 13vh;
    box-shadow: -2vmin 0 1.2050094998054566vmin currentColor;
}

.background span:nth-child(24) {
    color: #583C87;
    top: 68%;
    left: 15%;
    animation-duration: 349s;
    animation-delay: -349s;
    transform-origin: 22vw 21vh;
    box-shadow: -2vmin 0 0.31856072478297714vmin currentColor;
}

.background span:nth-child(25) {
    color: #E45A84;
    top: 80%;
    left: 47%;
    animation-duration: 180s;
    animation-delay: -217s;
    transform-origin: 3vw -1vh;
    box-shadow: 2vmin 0 1.029619956605243vmin currentColor;
}

.background span:nth-child(26) {
    color: #FFACAC;
    top: 31%;
    left: 100%;
    animation-duration: 431s;
    animation-delay: -409s;
    transform-origin: -12vw -14vh;
    box-shadow: 2vmin 0 0.30250328431185025vmin currentColor;
}

.background span:nth-child(27) {
    color: #E45A84;
    top: 15%;
    left: 90%;
    animation-duration: 391s;
    animation-delay: -4s;
    transform-origin: 9vw 8vh;
    box-shadow: -2vmin 0 1.2497291507679293vmin currentColor;
}

.background span:nth-child(28) {
    color: #FFACAC;
    top: 38%;
    left: 67%;
    animation-duration: 179s;
    animation-delay: -127s;
    transform-origin: 18vw -8vh;
    box-shadow: -2vmin 0 0.2607852868855898vmin currentColor;
}

.background span:nth-child(29) {
    color: #583C87;
    top: 73%;
    left: 28%;
    animation-duration: 46s;
    animation-delay: -244s;
    transform-origin: 23vw -5vh;
    box-shadow: 2vmin 0 0.5744598807153438vmin currentColor;
}

.background span:nth-child(30) {
    color: #FFACAC;
    top: 52%;
    left: 96%;
    animation-duration: 295s;
    animation-delay: -187s;
    transform-origin: 3vw -24vh;
    box-shadow: -2vmin 0 0.5668337165205541vmin currentColor;
}

.background span:nth-child(31) {
    color: #583C87;
    top: 14%;
    left: 33%;
    animation-duration: 443s;
    animation-delay: -306s;
    transform-origin: -17vw -8vh;
    box-shadow: 2vmin 0 0.9939295971843718vmin currentColor;
}

.background span:nth-child(32) {
    color: #E45A84;
    top: 56%;
    left: 74%;
    animation-duration: 127s;
    animation-delay: -320s;
    transform-origin: -20vw 0vh;
    box-shadow: 2vmin 0 0.8932093143150011vmin currentColor;
}

.background span:nth-child(33) {
    color: #E45A84;
    top: 55%;
    left: 27%;
    animation-duration: 304s;
    animation-delay: -433s;
    transform-origin: 5vw -8vh;
    box-shadow: 2vmin 0 0.29255530666612795vmin currentColor;
}

.background span:nth-child(34) {
    color: #583C87;
    top: 70%;
    left: 68%;
    animation-duration: 165s;
    animation-delay: -382s;
    transform-origin: -13vw -22vh;
    box-shadow: 2vmin 0 0.8951018554796004vmin currentColor;
}

.background span:nth-child(35) {
    color: #E45A84;
    top: 36%;
    left: 47%;
    animation-duration: 359s;
    animation-delay: -89s;
    transform-origin: 18vw 23vh;
    box-shadow: -2vmin 0 0.7250413084011658vmin currentColor;
}

.background span:nth-child(36) {
    color: #E45A84;
    top: 12%;
    left: 66%;
    animation-duration: 359s;
    animation-delay: -426s;
    transform-origin: 12vw -10vh;
    box-shadow: 2vmin 0 0.5382367053042516vmin currentColor;
}

.background span:nth-child(37) {
    color: #FFACAC;
    top: 36%;
    left: 83%;
    animation-duration: 296s;
    animation-delay: -247s;
    transform-origin: -8vw -16vh;
    box-shadow: -2vmin 0 0.5905612908211804vmin currentColor;
}

.background span:nth-child(38) {
    color: #E45A84;
    top: 27%;
    left: 65%;
    animation-duration: 316s;
    animation-delay: -42s;
    transform-origin: 0vw -10vh;
    box-shadow: 2vmin 0 0.6442313583377408vmin currentColor;
}

.background span:nth-child(39) {
    color: #583C87;
    top: 51%;
    left: 91%;
    animation-duration: 382s;
    animation-delay: -406s;
    transform-origin: 24vw -20vh;
    box-shadow: -2vmin 0 1.184318185193947vmin currentColor;
}

.background span:nth-child(40) {
    color: #583C87;
    top: 35%;
    left: 60%;
    animation-duration: 270s;
    animation-delay: -379s;
    transform-origin: 1vw -1vh;
    box-shadow: -2vmin 0 0.5930152709574077vmin currentColor;
}

.background span:nth-child(41) {
    color: #583C87;
    top: 89%;
    left: 72%;
    animation-duration: 252s;
    animation-delay: -397s;
    transform-origin: 4vw 12vh;
    box-shadow: -2vmin 0 0.303724066432437vmin currentColor;
}

.background span:nth-child(42) {
    color: #E45A84;
    top: 25%;
    left: 2%;
    animation-duration: 371s;
    animation-delay: -119s;
    transform-origin: -18vw -14vh;
    box-shadow: -2vmin 0 1.1555378204915219vmin currentColor;
}

.background span:nth-child(43) {
    color: #583C87;
    top: 93%;
    left: 36%;
    animation-duration: 40s;
    animation-delay: -394s;
    transform-origin: -23vw -18vh;
    box-shadow: -2vmin 0 0.4395781953354376vmin currentColor;
}

.background span:nth-child(44) {
    color: #FFACAC;
    top: 98%;
    left: 10%;
    animation-duration: 247s;
    animation-delay: -279s;
    transform-origin: 11vw 0vh;
    box-shadow: -2vmin 0 1.0121796182015077vmin currentColor;
}

.background span:nth-child(45) {
    color: #FFACAC;
    top: 70%;
    left: 85%;
    animation-duration: 9s;
    animation-delay: -108s;
    transform-origin: 7vw -24vh;
    box-shadow: -2vmin 0 0.5557207860451494vmin currentColor;
}

.background span:nth-child(46) {
    color: #FFACAC;
    top: 6%;
    left: 40%;
    animation-duration: 341s;
    animation-delay: -9s;
    transform-origin: 4vw -11vh;
    box-shadow: -2vmin 0 0.8476349487724522vmin currentColor;
}

.background span:nth-child(47) {
    color: #583C87;
    top: 8%;
    left: 90%;
    animation-duration: 173s;
    animation-delay: -162s;
    transform-origin: 18vw -19vh;
    box-shadow: 2vmin 0 0.821218888024688vmin currentColor;
}

.background span:nth-child(48) {
    color: #583C87;
    top: 21%;
    left: 68%;
    animation-duration: 123s;
    animation-delay: -5s;
    transform-origin: 24vw -12vh;
    box-shadow: -2vmin 0 0.25979825520633604vmin currentColor;
}

.background span:nth-child(49) {
    color: #E45A84;
    top: 60%;
    left: 70%;
    animation-duration: 70s;
    animation-delay: -232s;
    transform-origin: 4vw -21vh;
    box-shadow: -2vmin 0 1.2067809641290905vmin currentColor;
}
</style>
