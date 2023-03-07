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
}

.fade1{
background: linear-gradient(90deg, #E61835 0%, #F4D462 25%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

.dagens{
    background-color: #F4D462;
    border-radius: 25px;
    /* transparent ish */
    display: flex;
    flex-direction: column;
    width: 40%;
}

.hero{
  margin: 20px;
}

.dagens{
    padding: 20px;
}

p{
    font-size: larger;
    font-weight: 600;
    margin: auto;
    
}


</style>
    
<div class="content">

    <div class="header">
        <img src="hamar-katedralskole.svg" alt="Hamar katedralskole Logo">
        <h1 class="headerTxt">Kantina</h1>
    </div>
    <div class="hero">
        <h1 class="fade1 heroTxt">Dagens</h1>
        <div class="dagens">
            <img class="dagensImg" src="scampi.png" alt="image of food">
            <p>{data.Tirsdag}</p>    
        </div>
    </div>

</div>
