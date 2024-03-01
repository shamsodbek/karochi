<template >
 <div class="loader"></div>
</template>
<script>
window.addEventListener('load', ()=>{
    const loader = document.querySelector('.loader')
    loader.classList.add('active')
})
</script>
<style>
    .loader{
  position: fixed;  
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: black;
  transition: opacity 3s, visibility 1s ;
}
.loader.active{
  opacity: 0;
  visibility: hidden;
  
}
.loader::after{
  content: '';
  width: 85px;
  height: 85px;
  border: solid  black;
  border-top-color:  #0ef;
  animation: loader .8s ease infinite;
  border-radius: 50%;
  box-shadow:  var( --color1) 1px 0 10px,
    1px 0 10px,
    1px 0 10px,
    1px 0 10px,
    1px 0 10px,
    1px 0 10px,
    1px 0 10px;
}

@keyframes loader{
  0%{
    transform: rotate(0turn);
  }

  100%{
    transform: rotate(1turn);
  }
}

</style>