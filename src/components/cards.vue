<template>
    <h1>ANIMALS AND A CUTE KITTIE</h1>
    <div>
        <div id="show"></div>
    </div>
</template>

<script>
    async function fetchData(){
        const data = await fetch('https://rabiahaucha.github.io/JSON-SERVER/user.JSON')
        const jsonData = await data.json()
        const animals = jsonData.animals
        const show = document.querySelector('#show')
        // console.log(animals);

        animals.forEach( animals =>{
            show.innerHTML += `
            <div class="card" style="width: 18rem;">
  <img src="https://i.postimg.cc/6674GW3q/catss.jpg" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">${animals.species}</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
            
            `
        })
    }

    fetchData()
</script>

<style scoped>

</style>