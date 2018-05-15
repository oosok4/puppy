<template> 
   <section class="section"> 
     <div class="hero is-danger"> 
       <div class="hero-body"> 
         <div class="container"> 
           <h1 class="title is-1">PUPPY</h1> 
           <h2 class="subtitle">개사랑 사이트</h2> 
         </div> 
       </div> 
     </div> 
     <br> 
     <article class="message"> 
       <div class="message-header">개란 무엇인가?</div> 
       <div class="message-body">강아지를 구분하는 척도는 연령이므로 원래라면 크기에 관계없이 어린 개만을 강아지라고 부를 수 있다. 그러나 요즘에는 성견이라 할지라도 자신이 키우는 소형견을 강아지로 부르는 일도 자주있다.</div> 
     </article> 
     <div class="columns"> 
       <div class="column"> 
         <div class="container"> 
           <figure class="image is-squre"> 
             <img src="https://upload.wikimedia.org/wikipedia/commons/d/d9/Collage_of_Nine_Dogs.jpg" alt=""> 
           </figure> 
         </div> 
       </div> 
       <div class="column"> 
         <figure class="image is-squre"> 
           <img v-bind:src="image" alt=""> 
         </figure> 
       </div> 
     </div> 
   </section> 
 </template> 
 
 
 <script> 
   import axios from 'axios'; 
   export default { 
     data() { 
       return {}; 
     }, 
     async asyncData() { 
       const myImage = await axios.get('https://dog.ceo/api/breeds/image/random'); 
       return { image: myImage.data.message }; 
     } 
   }; 
 </script> 
