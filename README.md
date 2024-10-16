# Caja Interactiva en Vue

Este proyecto es un componente interactivo sencillo desarrollado en Vue 3 que permite configurar la apariencia de una caja de texto cambiando su color de fondo, color del texto, radio del borde, estilo de fuente, tamaño del texto y aplicando opacidad. Utiliza el sistema reactivo de Vue y enlaces con v-model para actualizar dinámicamente el componente en tiempo real.

# Demo
Puedes ver una demo en vivo en el siguiente enlace: [Demo]((https://template-rendering.netlify.app/))

## Tabla de Contenidos
- Instalación
- Características
- Uso
- Componentes
- Opciones de Personalización
- Licencia
- Instalación
- Para ejecutar este proyecto, asegúrate de tener Node.js y Vue CLI instalados.

1. Clona el repositorio:

```bash 
git clone https://github.com/tu-repositorio.git
```
2. Navega al directorio del proyecto:
```bash
cd tu-repositorio
```
3. Instala las dependencias:
```bash
npm install
```
4. Ejecuta el proyecto:
```bash
npm run serve
```


## Características
- Cambiar dinámicamente el color de fondo y el color del texto.
- Mostrar u ocultar el texto usando un checkbox.
- Modificar el radio del borde de la caja utilizando un control deslizante.
- Elegir entre varias fuentes para aplicar al texto.
- Ajustar el tamaño del texto mediante botones de opción (radio buttons).
- Aplicar opacidad a la caja a través de un checkbox.

## Uso
Una vez que el proyecto está en ejecución, puedes interactuar con el formulario del lado izquierdo para modificar los siguientes aspectos del cuadro interactivo en tiempo real:

1. Color de fondo: Ingresa un color válido o hexadecimal para cambiar el fondo del cuadro.
2. Color del texto: Ingresa un color para modificar el color del texto dentro del cuadro.
3. Mostrar u ocultar el texto: Marca o desmarca el checkbox para mostrar u ocultar el contenido textual.
4. Borde: Ajusta el rango del slider para modificar el radio del borde del cuadro.
5. Fuente del texto: Selecciona una fuente de la lista desplegable para aplicar al texto.
6. Tamaño del texto: Selecciona entre pequeño, mediano o grande para cambiar el tamaño de la fuente.
7. Opacidad: Marca el checkbox para aplicar opacidad al cuadro.


## Componentes
El proyecto utiliza un único componente Vue que contiene:

- Formulario de personalización: Permite ajustar las propiedades visuales del cuadro interactivo.
- Cuadro interactivo: Un div estilizado que cambia según los valores seleccionados en el formulario.

## Opciones de Personalización
Las siguientes opciones pueden personalizarse desde el formulario:

- Color de fondo: Puedes cambiar el color de fondo del cuadro introduciendo un valor de color en formato texto.
- Color del texto: Cambia el color del texto con un valor de color válido.
- Borde: Ajusta el radio de borde entre 10px y 500px.
- Contenido textual: Modifica el contenido textual de la caja a través de un campo de texto.
- Tipografía: Selecciona una fuente entre las opciones disponibles.
- Tamaño del texto: Elige entre tamaños predefinidos (pequeño, mediano, grande).
- Opacidad: Activa o desactiva la opacidad al marcar el checkbox correspondiente.

##  Licencia
Este proyecto está bajo la licencia MIT. Puedes consultarla en el archivo LICENSE del repositorio.