<script>
  export let data;
</script>



 <style>
   .discreetCard{
  border: solid 1px gray;
}
 </style>

 <section>
   <slot>
     <div class="discreetCard">
       <div class="card-body">
           <h5 class="card-title">{data}</h5>
       </div>
     </div>
   </slot>
 </section>
