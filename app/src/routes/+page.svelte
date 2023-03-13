<script>
    //run update script

    //grab info
    import data from "../meny.json"
    import { slide, fade, scale } from "svelte/transition"

    import { onMount } from 'svelte';

    let ready = false;
    onMount(() => setTimeout(()=>{ready = true}, 2000));

</script>

<style>

*{
    font-family: Arial, Helvetica, sans-serif;
}

:global(html){
    scroll-behavior: smooth;
}

:global(body){
    margin: 0;
    width: 100%;
}

.fade{
background: linear-gradient(90deg, #E61835 0%, #F4D462 40%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

.fade1{
background: linear-gradient(90deg, #E61835 0%, #F4D462 40%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

.fade2{
background: linear-gradient(90deg, #E61835 0%, #F4D462 120%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

.fade3{
background: linear-gradient(90deg, #F4D462 0%, #E61835 80%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

.header{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 20px;
}

.logo{
    align-items: center;
    justify-content: center;
    text-align: center;
    display: flex;
    flex-direction: column;
}

.underline{
    height: 1px;
    width: 25rem;
    background-color: rgb(255, 255, 255);
}

.headerTxt{
    margin: 10px 0px;
    font-size: 4rem;
    letter-spacing: 10px;
    color: white;
}

.landing{
    background-image: url(landingS.png);
    background-size:auto;
    background-repeat: no-repeat;
    background-position: right top;
    padding-bottom: 250px;
}

.hero{
    display:flex;
    justify-content:space-between;
}

.heroTxt{
    font-size: 6rem;
    margin-bottom: 0;
}

#rightHero{
    margin-right: 0px;
    display: flex;
    flex-direction: column;
    text-align: center;
}

#leftHero{
    margin-left: 80px;
    display: flex;
    flex-direction: column;
}

.dagensImg{
    height: 15rem;
    margin-top: 12rem;
    object-fit: contain;
}


p{
    font-size: 2rem;
    font-weight: 600;
    margin: 0;
}

.underlineFade{
    background: linear-gradient(90deg, #E61835 0%, #F4D462 90%);
    height: 0.7rem;
    width: 24rem;
    border-radius: 30px;
}

.desc{
    margin-top: 4rem;
    font-size: 4rem;
    margin-bottom: 0;
}

.btnFill{
    border-radius: 30px;
    background-color:#ef441d;
    opacity: 0.7;
    border-color: #ef441d;
    color: white;
    font-weight: 600;
    height: 4rem;
    width: 15rem;
    font-size: 2rem;
    margin-left: 5rem;
    border-style: solid
}

.btnOutline{
    border-radius: 30px;
    background-color:white;
    opacity: 0.7;
    border-color: #ef441d;
    color: #ef441d;
    font-weight: 600;
    height: 4rem;
    width: 10rem;
    font-size: 2rem;
    margin-left: 3rem;
    border-style: solid
}

.btnOutline:hover{
    border-radius: 30px;
    background-color:#ef441d;
    opacity: 0.7;
    border: none;
    color: white;
    font-weight: 600;
    height: 4rem;
    width: 10rem;
    font-size: 2rem;
    margin-left: 3rem;
    border-style: solid
}

.btnFill:hover{
    border-radius: 30px;
    background-color:white;
    opacity: 0.7;
    border-color: #ef441d;
    color: #ef441d;
    font-weight: 600;
    height: 4rem;
    width: 15rem;
    font-size: 2rem;
    margin-left: 5rem;
    border-style: solid
}

#footbar{
    padding: 20px;
    background-color: rgba(238, 198, 58, 0.7);
    color: black;
    display:flex;
    flex-direction: column;
    text-align: center;
}

.nyheter{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.banner{
    background-image: url(nyhet.png);
    background-repeat: no-repeat;
    background-size: contain;
    text-align: center;
    color: white;
    margin: 30px;
    margin-left: 60px;
}

.produkt{
    height: 25rem;
    margin: 40px;
    margin-bottom: 0;
}

.tba{
    background-color: white;
    height: 400px;
    width: 400px;
    margin: 30px;
}

#meny{
    margin: 50px 100px;
    display: flex;
    flex-direction: row;
    align-items: start;
    justify-content: space-between;
}

.redLine{
    background-color: #E61835;
    height: 20rem;
    width: 0.5rem;
    border-radius: 30px;
    margin: 10px;
}

.menyHead{
    font-size: 6rem;
    margin: 5px;
    text-align: right;
}

.menyHeadBox{
    display:flex;
    align-items:center;
    margin-left:16rem;
}

.menyBox{
    background-color:#ECECEC;
    border-radius: 30px;
    box-shadow: 4px 4px 4px grey;
    max-width: 700px;
}

.dag{
    background-color: rgba(239, 68, 29, 0.6);
    border-radius: 30px;
    display: flex;
    margin: 40px;
    width: 75%;
    padding: 30px;
    color: black;
    margin-top:5px;
}

.dagHead{
    font-size: 3rem;
    margin: 10px;
    margin-left: 60px;
}

.line{
    background-color: black;
    border-radius: 30px;
    height: 6rem;
    width: 5px;
}

.icon{
    height: 50px;
    width: 50px;
    margin: 10px;
}

.opening{
    background-color: white;
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    min-height: 100vh;
}

.ring{
    position: absolute;
    width:200px;
    height: 200px;
    border-radius: 50%;
    animation: ring 2s linear infinite;
}

@keyframes ring{
    0%{
        transform: rotate(0deg);
        box-shadow: 1px 5px 2px #E61835;
    }
    50%{
        transform: rotate(180deg);
        box-shadow: 1px 5px 2px #F4D462;
    }
    100%{
        transform: rotate(360deg);
        box-shadow: 1px 5px 2px #ef441d;
    }
}

.ring:before{
    position:absolute;
    content: "";
    left: 0;
    right: 0;
    top: 0;
    height: 100%;
    width:100%;
    border-radius: 50%;
    box-shadow: 0 0 5px rgba(255, 255, 255, 0.3);
}

@media screen and (max-width:1050px){
    .menyHeadBox{
    display:flex;
    align-items:center;
    margin: 0;
    max-width: 385px;
    }

    .hero{ 
    display:flex;
    justify-content:space-between;
    flex-direction:column
    }

    #meny{
    margin: 40px 0px;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: space-between;
    }

    .produkt{
    height: 12rem;
    margin: 40px;
    margin-bottom: 0;
    }

    .buttons{
        display: none !important;
    }

    .fade{
    background: linear-gradient(90deg, #fff 0%, #fff 40%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    }

    .underlineFade{
    background: linear-gradient(90deg, #fff 0%, #fff 90%);
    height: 0.7rem;
    width: 18rem;
    border-radius: 30px;
    }

    
    .headerTxt{
        margin: 10px 0px;
        font-size: 2rem;
        letter-spacing: 10px;
        color: white;
    }

    .underline{
    height: 1px;
    width: 10rem;
    background-color: rgb(255, 255, 255);
    }

    .heroTxt{
    font-size: 4rem;
    margin-bottom: 0;
    }

    .desc{
    margin-top: 2rem;
    font-size: 2rem;
    margin-bottom: 0;
    }

    .dagHead{
    font-size: 2rem;
    margin: 10px;
    margin-left: 60px;
    }

    .dag{
    background-color: rgba(239, 68, 29, 0.6);
    border-radius: 30px;
    display: flex;
    margin: 20px;
    width: 75%;
    padding: 30px;
    color: black;
    margin-top:5px;
    }
}

span{
    color: #E61835;
    font-size: 20px;
    text-transform: uppercase;
    letter-spacing: 3px;
    line-height: 200px;
}

</style>


{#if !ready}
<div class="opening">

    <div class="ring">
        <span></span>
    </div>
    <h1 class="fade2">Kantina</h1>

</div>
{/if}

{#if ready}
<div class="landing">

    <div class="header">
        <img src="hamar-katedralskole.svg" alt="Hamar katedralskole Logo">
        <div transition:slide class="logo">
            <h1 class="headerTxt">Kantina</h1>
            <div class="underline"></div>
        </div>
        
    </div>
    
    <div class="hero">
        <div transition:slide id="leftHero">
            <h1 class="fade heroTxt">Torsdag</h1>
            <div class="underlineFade"></div>
            <h1 class="desc">{data.Torsdag}</h1>
            <p style="margin:20px; margin-left:0;">(melk)</p>    
        </div>  
        <div transition:fade id="rightHero">
            <img class="dagensImg" src="scampi.png" alt="image of food">
        </div>
    </div>

    <div class="buttons" transition:fade style="display:flex; margin-top:20px;">
        <a href="#meny"><button class="btnFill">Uke meny</button></a>
        <a href="#footbar"><button class="btnOutline">info</button></a>
    </div>
</div>

<div class="nyheter"> 
    <div class="banner">
        <img class="produkt" src="noisy.png" alt="noisy (kullsyreholdig leskedrikk)">
        <h1 style="margin-top: 0;">Noisy Mango</h1>
    </div>
    
    <div class="tba"></div>



</div>

<div id="meny">
    <div class="menyHeadBox">
        <div>
            <h1 class="menyHead fade3">Meny</h1>
            <h1 class="menyHead fade3">uke 10</h1>
        </div>
        <div class="redLine"></div>
    </div>
    
        
    <div class="menyBox">
        
        <h1 class="dagHead fade1">Mandag</h1>
        <div class="dag"><p>{data.Mandag}</p></div>
        
        <h1 class="dagHead fade1">Tirsdag</h1>
        <div class="dag"><p>{data.Tirsdag}</p></div>
        
        <h1 class="dagHead fade1">Onsdag</h1>
        <div class="dag"><p>{data.Onsdag}</p></div>
        
        <h1 class="dagHead fade1">Torsdag</h1>
        <div class="dag"><p>{data.Torsdag}</p></div>
        
        <h1 class="dagHead fade1">Fredag</h1>
        <div class="dag"><p>{data.Fredag}</p></div>
    </div>
    
</div>

<div id="footbar">

    <div style="display:flex; justify-content:space-between;">
        <div>
            <div style="display:flex; justify-content:center;">
                <div class="icon"><img src="twitter.svg" alt="twitter"></div>
                <div class="icon"><img src="instagram.svg" alt="instagram"></div>
                <div class="icon"><img src="facebook.svg" alt="facebook"></div>
            </div>
            <div>
                <p>Følg oss på Sosiale medier</p>
            </div>
        </div>

        <div class="line"></div>

        <div>
            <p>info goes header</p>
        </div>

    </div>

    <div>
        <p style="font-size: 1rem; margin-top:30px;">Simen og Leon 2023</p>
    </div>

</div>
{/if}