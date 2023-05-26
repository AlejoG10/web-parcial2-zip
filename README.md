# Instrucciones para la Ejecución

## Instrucciones Front-End (React JS)
1. Descargar el archivo `parcial2.zip` y descomprimirlo
2. Instalar las dependencias del proyecto con:

	> npm install

3. Correr el front con el comando
	> npm start

## Instrucciones Back-End (Nest JS)
 1. Descargar el proyecto para correr el back localmente
 2. Cambiar el método `bootstrap()` en el archivo `main.ts` de la siguiente manera:
 
	Cambiar el puerto de la aplicación de `3000` a `8000`
	> await app.listen(8000);

	Habilitar el cors agregando la siguiente línea de código
	> app.enableCors();

3. Correr el back con el comando
	> npm start

# Reporte de las Decisiones

## Dependencias Adicionales Incluidas

1. TailwindCSS: Librería para utilizaer estilos de `CSS` y que reemplaza los archvivos `CSS` y el uso de la librería `Bootstrap`
2. Axios: Librería para hacer los requests `(GET, POST, PUT, DELETE)` al back y que reemplaza la librería de JavaScript `fetch`

## Estructura de la Aplicación

- La aplicación cuenta con 2 vistas: El login, en la ruta: `/` y la grilla de libros y detalle de los mismos en la ruta `/home`.
- El contenido de la página `<Login />` se puede encontrar en la ruta `/src/pages/Login.jsx` y no cuenta con componentes adicionales, todos los elementos `HTML` son creados dentro del archivo.
- El contenido de la página `<Home />` se puede encontrar en la ruta `/src/pages/Home.jsx`. Entre su contenido se llama al componente personalizado `<Card />` (ubicado en la ruta `/src/components/Card.jsx`) con los props: `id, name, image, isbn y handleClick`. En donde: `id`: es el id del libro, `name`: es el nombre del libro, `image`: es la imagen del libro, `isbn`: es el isbn del libro y `handleClick`: es una función que maneja la lógica para mostrar el detalle del libro al que se le hizo click.
