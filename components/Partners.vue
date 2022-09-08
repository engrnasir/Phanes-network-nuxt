<template>
  <div class=" parteners">
    <img src="@/assets/partnersbg.png" class="bg" alt="">
    <div class="row">
        <h2 class="heading">Our Partners</h2>
        <div class="partner-icons" >
            <img src="@/assets/partner1.png" alt="" :id="`partnerIcon${0}`" class="icon">
            <img src="@/assets/partner2.png" alt="" :id="`partnerIcon${1}`" class="icon">
            <img src="@/assets/partner3.png" alt="" :id="`partnerIcon${2}`" class="icon">
            <img src="@/assets/partner4.png" alt="" :id="`partnerIcon${3}`" class="icon">
            <img src="@/assets/partner5.png" alt="" :id="`partnerIcon${4}`" class="icon">
            <img src="@/assets/partner6.png" alt="" :id="`partnerIcon${5}`" class="icon">
        </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            partners : ['partner1.png','partner2.png','partner3.png','partner4.png','partner5.png','partner6.png',]
        }
    }

}
</script>

<style lang="scss" scoped>
    .parteners{
        position: relative;
        margin-bottom: 157px;
        background-color: #011e15;
        background-image: linear-gradient(rgba(0, 3, 2, 0.75),rgba(0, 3, 2, 0.75));
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        
        overflow: hidden;
        -webkit-perspective: 240px;
        perspective: 240px;
        .bg{
            position: absolute;
            top: -100px;
            left: -100px;
            width: 3000px;
            min-height: 600px;

            @media only screen and (max-width:1600px){
                width: 2000px;
            }
            @media only screen and (max-width:1200px){
                width: 1600px;
            }
            @media only screen and (max-width:580px){
                width: 900px;
            }

            background-image: linear-gradient(rgba(0, 3, 2, 0.75),rgba(0, 3, 2, 0.75));
            -webkit-transform: rotateX(20deg);
            -webkit-perspective-origin: center; 
            
            -webkit-animation: moveSquare 12s infinite ease-in-out alternate;
            animation: moveSquare 12s infinite ease-in-out alternate;
            opacity: .5;
        }

        @keyframes moveSquare {
            0% {
                // -webkit-transform: translateX(0px) translateY(-40px) rotateX(0deg);
                transform: translateX(-250px) translateY(-100px) rotateX(0deg);
                opacity: .5;
            }
            0% {
                // -webkit-transform: translateX(0px) translateY(-40px) rotateX(0deg);
                transform: translateX(-100px) translateY(-50px) rotateX(0deg);
                opacity: .1;
            }
            100% {
                // -webkit-transform:translateX(-100px) translateY(-70px) rotateX(20deg);
                transform:translateX(-250px) translateY(-100px) rotateX(20deg);
                opacity: .5;
            }
        }




        .row{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 96px;
            @media only screen and (max-width: 780px){
                padding: 30px 40px;
                margin-bottom: 30px;
            }
            .heading{
                font-weight: 800;
                font-size: 48px;
                line-height: 59px;
                margin-bottom: 74px;
                @media only screen and (max-width: 780px){
                    font-size: 36px;
                    text-align: center;
                    margin-bottom: 30px;
                    width: max-content;
                }
            }
            .partner-icons{
                z-index: 2;
                display: flex;
                justify-content: center;
                align-items: center;
                @media only screen and (max-width:1260px) {
                    width: 100%;
                    display: grid;
                    grid-template-columns: repeat(3,1fr);
                    gap: 37px;
                    justify-items: center;  
                }
                @media only screen and (max-width:780px) {
                    grid-template-columns: repeat(2,1fr);
                }
                &>*:not(:last-child){
                    margin-right: 50px;
                    @media only screen and (max-width:1260px) {
                        margin-right: 0;
                    }
                }
                .icon{
                    height: 50px;
                    @media only screen and (max-width:780px) {
                        height: 30px;
                    }
                }
                #partnerIcon2{
                    height: 29.8px;
                    @media only screen and (max-width:780px) {
                        height: 22px;
                    }
                }
                #partnerIcon5{
                    height: 40px;
                    @media only screen and (max-width:780px) {
                        height: 25px;
                    }
                }
            }

        }
    }

</style>