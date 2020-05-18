<script>
  import { fly} from 'svelte/transition';


</script>


<div class="container" in:fly="{{x:-300, duration: 600}}">

<h1 ><span>Virtual</span> Buddy</h1>
<h2>Service</h2>

<div class="card">
<div class="card-content">
 <i class="fab fa-grav"></i>

 <p>Acompañamiento Virtual para tu vida. </p>
 <i class="fas fa-globe-americas" ></i>
 <p>Desde Argentina para cualquier lugar del mundo</p>
 
  <div class="btn">Comprar</div>

</div>

</div><br><br>
</div>

<style>

i {
  font-size: 90px;
  margin-top: 15px;
  margin-bottom: 10px;
}

.container {
    text-align: center;
    margin-top: 20px;
     font-weight: normal;
     color: #333;
    margin-bottom: 20px;
}
.container h1, h2 {
       font-family: "Satisfy", cursive;

}
.container h2 {
         font-family: "Satisfy", cursive;
         color: rgba(78, 158, 250, 0.795);

}

.container span {
  color: rgba(78, 158, 250, 0.795);

}

.card {
      width: 270px;
      margin: 10px auto;
     font-family: "Comfortaa", cursive;
     background:  rgba(78, 158, 250, 0.192);


  }
  .card p {
    padding: 10px;
    margin-bottom: 20px;
    margin-top: 10px;
  }

  .btn {
    background:rgba(78, 158, 250, 0.733);
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    border: 2px solid rgb(78, 158, 250);
    border-radius: 5px;
    font-weight: bold;
  }
 
     
</style>