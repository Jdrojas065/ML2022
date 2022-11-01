<template>
   <body>
    
   
    <div >
        
       <h1>Comanda</h1>
       <input type="text" v-model="newNombre"   v-on:keypress.enter="nuevoFila()"  >
       <input type="text" v-model="Canti"  v-on:keypress.enter="nuevoFila()" >
       <input type="text" v-model="Codigoes"  v-on:keypress.enter="nuevoFila()" >
       <input type="text" v-model="Valors"  v-on:keypress.enter="nuevoFila()" >
       <input type="text" v-model="pago"  v-on:keypress.enter="nuevoFila()" >
       <input type="text" v-model="emple"  v-on:keypress.enter="nuevoFila()" >
       <input type="text" v-model="Des"  v-on:keypress.enter="nuevoFila()" >
       <input type="text" v-model="eda"  v-on:keypress.enter="nuevoFila()" >
       <hr>

       <div class="contenedor" >
        <center>
           <table border="5" >
            
           <thead>
               <tr class="columnas">
               <td>Numero</td>
               <td>Producto</td>
               <td>Cantidad</td>
               <td>Codigo</td>
               <td>Valor</td>
               <td>Metodo de pago</td>
               <td>Empleado</td>
               <td>Descripcion</td>
               <td >Edad</td>
               <td >Descuento</td>
              
            </tr>
           </thead>
   
               <tbody>
                   <tr class="columnas" v-for="({Nombre,Codigo,Valor,Metodo,Empleado,Cantidad,Descripcion,Edad},index) in product" :key="index">
                       <td>{{index+1 }}</td>
                       <td>{{Nombre}}</td>
                       <td>{{Codigo}}</td>
                       <td>{{Valor}}</td>
                       <td>{{Metodo}}</td>
                       <td>{{Empleado}}</td>
                       <td>{{Cantidad}}</td>
                       <td>{{Descripcion}}</td>
                       <td>{{Edad}}</td>
                       <!-- <td v-if="Nombre === 'Hamburguesa'">Si Esta Hamburguesa</td>
                       <td v-else>No esta</td> -->
                       <td v-show="Edad <= 18">"Usted tiene descuento 5%"</td>
                       
                </tr>
           
           </tbody>
   
           </table>    
        </center>
           
       
         </div>
    </div>    
</body>
   
   </template>
   
   <script>
       const product=[
           {Nombre: 'Hamburguesa' , Codigo: '#45', Valor:'$10.000',Metodo:'Efectivo',Empleado:'1',Cantidad:'2',Descripcion:'sin cebolla',Edad:'16'},
       ]
       console.log(product)
    export default{
      data(){
       return {product,
           newNombre: "Producto",
           Canti:"Cantidad",
           Codigoes:"Codigo",
           Valors:"Valor",
           pago:"Metodo de Pago",
           emple:"Empleado",
           Des:"Descripcion",
           eda:"Año de Nacimiento"
       }
      },
      methods:{
        nuevoFila(){
           console.log("dio enter")
           this.product.unshift({
               Nombre:this.newNombre,
               Codigo:this.Codigoes,
               Valor:this.Valors,
               Metodo:this.pago,
               Empleado:this.emple,
               Cantidad:this.Canti,
               Descripcion:this.Des,
               Edad:2022-this.eda
   
           })
   
        }
      }
      
     }
   
   </script>
   
   <style>
   h1 {
    text-align: center;
    font-size: 75px;
    font-family: 'Tahoma'
}
h1 {
    margin-top: 0;
    margin-bottom: 2rem;
    font-weight: 300; }
  h1 { font-size: 4.0rem; line-height: 1.2;  letter-spacing: -.1rem;}
  .contenedor {
    margin: 30px 0;
}






    h1{
        color: blue;
    }
    thead{
        background-color: rgb(255, 94, 0);
    }
    table{
      background-color: rgb(255, 214, 34);
    }
   .contenedor{
       
       display: inline-bock;
       ;
   }
   .columnas{
       text-align: center;
       
   }
   hr{
    border: 5px solid rgb(252, 32, 3);
   }
   
body{
    background-color: rgba(255, 136, 9, 0.542);
}
text{
    background-color: aliceblue;
}
   </style>