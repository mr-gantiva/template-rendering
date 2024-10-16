<script setup>
import { ref } from 'vue'

const colorFondo = ref('black')
const colorTexto = ref('white')
const show = ref(true);
const bordeCaja = ref(0)
const contenido = ref('Awesome Vue.js')
const color = ref('black')

const tipografia = ref('')
const tipografias = ref(["Arial", "Courier New", "Georgia", "Times New Roman", "Verdana"])
const aplicarOpacidad = ref(false)
const tamanio = ref('')
</script>

<template>
  <section class="container contenedor__ppal py-5">
    <div class="row">
      <!--Formulario-->
      <div class="col-12 col-md-6 mb-5">
        <div class="contenedor-formulario p-5">

          <!-- Cambiar el color de fondo -->
          <div class="mb-3">
            <label for="colorFondo" class="form-label">Color de fondo</label>
            <input type="text" class="form-control" id="colorFondo" v-model='colorFondo' placeholder="black">
          </div>

          <!-- Cambiar el color del texto -->
          <div class="mb-3">
            <label for="colorTexto" class="form-label">Color del texto</label>
            <input type="text" class="form-control" id="colorTexto" placeholder="white" v-model='colorTexto'>
          </div>

          <!-- Mostrar el texto -->
          <div class="form-check mb-3">
            <input class="form-check-input" type="checkbox" value="" id="showTexto" v-model="show" checked>
            <label class="form-check-label" for="showTexto">
              Mostrar Texto
            </label>
          </div>

          <!-- Borde de la caja -->
          <div class="check__box mb-3">
            <label for="bordeCaja" class="form-label">Borde</label>
            <input type="range" class="form-range" id="bordeCaja" min="10" max="500" v-model="bordeCaja">
          </div>

          <!-- Contenido textarea -->
          <div class="form mb-4">
            <label for="contenido">Contenido Textual:</label> -->
            <textarea class="form-control" placeholder="" id="contenido" v-model="contenido"></textarea>
          </div>

          <!-- Tipografia -->
          <select class="form-select mb-4" v-model="tipografia">
            <option v-for="fuente in tipografias">{{ fuente }}</option>
          </select>

          <!-- Opacidad -->
          <div class="form-check mb-3">
            <label class="form-check-label" for="opacityBox">
              Opaco
            </label>
            <input class="form-check-input" type="checkbox" value="" id="opacityBox" v-model="aplicarOpacidad">
          </div>

          <!-- Tamaño texto -->
          <p>Tamaño de letra</p>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio1" value="16px"
              v-model="tamanio">
            <label class="form-check-label" for="inlineRadio1">Pequeño</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio2" value="32px"
              v-model="tamanio">
            <label class="form-check-label" for="inlineRadio2">Mediano</label>
          </div>
          <div class="form-check form-check-inline">
            <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio3" value="64px"
              v-model="tamanio">
            <label class="form-check-label" for="inlineRadio3">Grande</label>
          </div>

        </div>
      </div>

      <!-- Cuadro interactua -->
      <div class="col-12 col-md-6 mb-5 d-flex justify-content-center align-items-center">
        <div class="contenedor__cuadro d-flex justify-content-center align-items-center"
          :style="{ background: colorFondo, borderRadius: bordeCaja + 'px', opacity: aplicarOpacidad ? 0.2 : 1 }">
          <h4 :style="{ color: colorTexto, fontFamily: tipografia, fontSize: tamanio }" v-if="show">{{ contenido }}</h4>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contenedor__ppal {
  width: 100%;
  /* height: 100vh; */
  display: flex;
  align-items: center;
}

label {
  color: #fff;
}

.row {
  width: 100%;
}

.contenedor-formulario {
  width: 100%;
  background: #202b38;
}

.contenedor__cuadro {
  width: 300px;
  height: 300px;
  background-color: bgColor;
}

.text-white {
  color: white;
}
</style>
