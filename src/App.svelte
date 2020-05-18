<script>
  import { fly, fade} from 'svelte/transition';
  import Programacion from './Programacion.svelte';
  import Back from './Back.svelte'
  import Compañia from './Compañia.svelte'


  let programacion = false
  let compañia = false

  const showProgramacion = () => {
	  programacion = !programacion
  }
  const showCompañia = () => {
	  compañia = !compañia
  }

</script>


{#if programacion == false && compañia == false}

<div class="container"  in:fade>
<div class="containerImg"><img src="./img/en.jpg" alt=""></div>
<h1><span>Enzo</span> Daneri</h1>

<div class="btnUno" on:click={showProgramacion}>Programación</div>
<div class="btnDos" on:click={showCompañia}>Virtual Buddy</div>
<div class="btnTres">Metas App</div>


  <footer>
   <div class="footerCont">
    <span >Contacto</span>
    <span ><i class="fas fa-check"></i> Tips</span>
    <span >Info</span>
   </div>
   </footer>

</div>
{/if}

{#if programacion == true}
<Programacion on:click={showProgramacion}/>
<Back on:click={showProgramacion}/>

{/if}

{#if compañia == true}
<Compañia on:click={showCompañia}/>
<Back on:click={showCompañia}/>

{/if}

<style>
.container {
	text-align: center;
	padding-left: 25px;
	padding-right: 25px;
	margin-top: 35px;
}

.container h1 {
	font-family: "Satisfy", cursive;
	font-weight: normal;
	font-size: 50px;
	color: #333;
	margin: 20px;
}
.container span {
	color: rgba(78, 158, 250, 0.897);
}
.container img {
	border-radius: 50%;
	width: 100px;
}

.btnUno {
	width: 270px;
	height: 60px;
	background: rgba(51, 51, 51, 0.959);
	margin: 10px auto;
	border-radius: 5px;
	cursor: pointer;
	display: flex;
	align-items: center;
	justify-content: center;
	color: #fff;
	font-family: "Comfortaa", cursive;
	font-size: 20px;

}
.btnDos {
	width: 270px;
	height: 60px;
	background: rgba(51, 51, 51, 0.959);
	margin: 10px auto;
	border-radius: 5px;
	cursor: pointer;
	display: flex;
	align-items: center;
	justify-content: center;
	color: #fff;
	font-family: "Comfortaa", cursive;
	font-size: 20px;
}
.btnTres {
	width: 270px;
	height: 60px;
	background: #333;
	margin: 10px auto;
	border-radius: 5px;
	cursor: pointer;
	display: flex;
	align-items: center;
	justify-content: center;
	color: #fff;
	font-family: "Comfortaa", cursive;
	font-size: 20px;
}


footer {
  text-align: center;
  margin-top: 60px;
  font-family: "Comfortaa", cursive;
  margin-bottom: 30px;
  color: var(--textColor);

}
 
 .footerCont {
   text-align: center;
 }


footer span {
    cursor: pointer;
	margin: 20px;
}

</style>