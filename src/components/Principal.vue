<template>

  <section class="src-components-principal">
    
  
    <span>Color: <input type="text" v-model="color"/></span>
    <span>Fondo: <input type="text" v-model="fondo"/></span> 
    <span>Size: <input type="number" v-model="size"/></span> 
    <hr>
    <span>Texto: <input type="text" :style="estilo(color, fondo, size)" v-model="texto" /> </span>
    <hr>
    <span>Cantidad de palabras: {{contadorPalabras}} </span>
    <hr>
    <div class="jumbotron">
      <table class="table">
         
          <tr>
            <th scope="col">Pregunta</th>
            <th scope="col">Respuesta</th>
          </tr>
        
        <tbody>
          <tr>
            <th scope="col">1 ¿Qué es Axios?</th>
            <th scope="col">B</th>
          </tr>
                    <tr>
            <th scope="col">2 Con Axios se pueden implementar los verbos</th>
            <th scope="col">C</th>
          </tr>
                    <tr>
            <th scope="col">3 ¿Que es Vuex?</th>
            <th scope="col">B</th>
          </tr>
                    <tr>
            <th scope="col">4 Las acciones en su implementación permiten lógica</th>
            <th scope="col">D</th>
          </tr>
                    <tr>
            <th scope="col">5 Las mutaciones</th>
            <th scope="col">D</th>
          </tr>
        </tbody>
      
      </table>
    </div>

  </section>

</template>

<script >

  export default  {
    name: 'src-components-principal',
    props: [],
    mounted () {

    },
    data () {
      return {
        color:"",
        fondo:"",
        size:"",
        texto:""
      }
    },
    methods: {
      estilo(color, fondo, size){
        return {
          color: color,
          backgroundColor: fondo,
          fontSize: size + "px"
        }
      }
    },
    computed: {
      contadorPalabras(){
        let cant = this.texto.trim(this.texto.replace(/ +(?= )/g,'')).split(' ')
        return cant.length
      }
    }
}


</script>

<style scoped lang="css">
  .src-components-principal {

  }
</style>
