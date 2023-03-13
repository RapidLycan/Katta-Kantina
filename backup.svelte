<script>
    //run update script

    //grab info
    import data from "../meny.json"

</script>

<style>

*{
    font-family: Arial, Helvetica, sans-serif;
}

:global(body){
    margin: 0;
}

.header{
    box-shadow: 2px 0 10px black;
    display: flex;
    justify-content: space-between;
    padding: 0px 20px;
}

.headerTxt{
    font-size: 2rem;
}

.heroTxt{
    font-size: 5rem;
    margin: 20px;
    left: -32rem;
    position:relative;
    color: #E61835;
}

.fade1{
background: linear-gradient(90deg, #E61835 0%, #F4D462 70%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

.dagens{
    background: linear-gradient(180deg, #E61835 0%, #F4D462 90%);
    border-radius: 25px;
    /* transparent ish */
    display: flex;
    flex-direction: column;
    width: 40%;
}

.hero{
  margin: 60px;
  align-items: center;
  display: flex;
  flex-direction: column;
}

.dagens{
    padding: 0px 60px;
    height: 30rem;
    width: 80rem;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}

.dagensImg{
    width: 30rem;
}

.bakeImg{
    width: 20rem;
}

.slice{
    z-index: 1;
    background-color: white;
    width: 40px;
    height: 600px;
    rotate: 25deg;
    position: relative;
}

.bakevare{
    text-align: center;
}

.ukeMeny{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.dag{
    display: flex;
    position: relative;
    left: -200px;
    margin: 20px;
    border-radius: 30px;
    background-color: lightgrey;
    width: 60%;
    height: 5rem;
    text-align: center;
    justify-content: center;
    align-items: center;
}

.dag p{
    color: black;
    text-shadow: none;
}

p{
    font-size: x-large;
    font-weight: 600;
    margin: auto;
    color: white;
    text-shadow: 2px 2px 2px black;
}

/* .opening{

} */


</style>
    
<div class="content">

    <div class="header">
        <img src="hamar-katedralskole.svg" alt="Hamar katedralskole Logo">
        <h1 class="headerTxt">Kantina</h1>
    </div>
    <div class="main">
        <div class="hero">
            <h1 class="heroTxt">Torsdag</h1>
            <div class="dagens">
                <div>
                    <img class="dagensImg" src="scampi.png" alt="image of food">
                    <p>{data.Torsdag}</p>    
                </div>
                <div class="slice"></div>
                <div class="bakevare">
                    <img class="bakeImg" src="brownie.png" alt="brownie goes here">
                    <p>bakevare</p>
                </div>
            </div>
        </div>
        <div class="ukeMeny">
        <h1>Meny #uke</h1>
        <div class="dag"><p>{data.Mandag}</p></div>
        <div class="dag"><p>{data.Tirsdag}</p></div>
        <div class="dag"><p>{data.Onsdag}</p></div>
        <div class="dag"><p>{data.Torsdag}</p></div>
        <div class="dag"><p>{data.Fredag}</p></div>
        
        </div>
    </div>
</div>

<div class="opening">
    
</div>
