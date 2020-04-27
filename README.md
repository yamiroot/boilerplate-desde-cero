# Boilerplate-desde-cero
Aprender a configurar tu entorno de trabajo desde cero.

## Paso N°1:
Crear carpetas de trabajo. 

* src: 
 Carpeta principal. Está carpeta contendrá todos nuestros archivos de trabajo. 
 Como estructura básica se sugiere que contenga tres carpetas básicas de 
 nombres: `css`, `js` e `img`; y un archivo "index.html".

## Paso N°2:
Crear archivo `package.json`. Este archivo contiene información acerca de 
nuestra proyecto y además, guarda un registro de las dependencias utilizadas.
Este archivo no debe estar incluido en la carpeta "src".

Existen dos formas de crear nuestro `package.json`, la primera es de forma 
manual y la segunda es por medio del comando `npm init`. 

Si aún no sabe como crear un archivo `package.json`, puedes dar click 
[aquí](https://medium.com/noders/t%C3%BA-yo-y-package-json-9553929fb2e3). Te 
adjuntamos, además, la documentación oficial de `npm` acerca de 
[cómo crear este archivo](https://docs.npmjs.com/creating-a-package-json-file).

#### Observación
Al crear nuestro `package.json` utilizando el comando `npm init` nos pedirá un 
`entry point` o punto de entrada. El **punto de entrada** es el archivo javascript
que se invocará cuando los consumidores de su módulo lo "requieran", este archivo 
incluirá la lógica principal de su módulo.

Si nuestro proyecto fuera una librería, nuestro `entry point` debería ser un archivo
de extensión `.js`. En cambio, en un proyecto web debería ser un archivo de extensión 
`.html`. Cabe recalcar que en éste último deberán cargarse los módulos de la lógica 
de nuestro proyecto.

Puede ver más información acerca de este apartado 
[aquí](https://stackoverflow.com/questions/32800066/what-is-entry-point-in-npm-init).

## Paso N°3:
Instalar la dependencia `serve` de `npm`. Este paquete nos va a permitir correr el 
servidor con el comando `npm start`.

Además, `serve` nos proporciona una interfaz ordenada que enumera los contenidos de
nuestro directorio.

Puede ver la documentación oficial de este paquete [aquí](https://www.npmjs.com/package/serve).

## Paso N°4:
Configurar el script `start` en nuestro `package.json`. No olvide especificar correctamente
la ruta de la carpeta contenedora de nuestros archivos.

```
"scripts": {
    "start": "serve ./src"
}
```

## Paso N°5:
Si todo ha ido bien, deberías poder arrancar el servidor web usando el comando `npm start` 
y con ello, dirígete a `http://localhost:5000` en tu navegador para poder ver la interfaz 
de tu programa.

A codear se ha dicho! :rocket:

