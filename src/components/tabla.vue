<template>
  <div>
      <table :class="clases">
        <caption v-if="!!subtitulo"> {{subtitulo}} </caption>
        <thead>
          <tr>
            <th scope="col" v-for="(item, i) in titulos" :key="i">{{item}}</th>            
          </tr>
        </thead>
        <tbody>
          <tr v-for="(fila, ii) in filas" :key="ii">
            <td v-for="(dato, iii) in fila" :key="iii"> {{dato}}</td>
          </tr>
        </tbody>
      </table>
    </div>
</template>

<script>
export default {
  name: 'HectorTabla',
  props: {
    subtitulo: String,
    titulos: {
      type: Array,
    },
    filas: {
      type: Array,
    },
    clases: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>
