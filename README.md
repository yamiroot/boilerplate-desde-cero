<h1 align="center">Boilerplate-desde-cero</h1>
Aprender a configurar tu entorno de trabajo desde cero.

## Paso N°1:
Definir estructura del proyecto. Puedes tomar opcionalmente la siguiente estructura:

* src: 
 Carpeta de trabajo. Como estructura básica se sugiere que contenga tres carpetas de 
 nombres: `css`, `js`, `img` y un archivo `index.html`.
 
  - `index.html:` Es el archivo que el servidor ejecuta por defecto cuando carga tu 
  dominio.
  
  - En informática **SRC** como acrónimo significa Set Redundancy Compression. Son
  métodos de compresión de datos para representar una determinada información empleando 
  una menor cantidad de espacio.

## Paso N°2:
Crear archivo `package.json`. Este archivo no debe estar incluido en la carpeta "src".

En resumen, este archivo contiene información acerca de:
 - Todos los módulos necesarios para su proyecto y sus versiones instaladas.
 - Todos los metadatos de un proyecto, como el autor y la licencia, entre otros.
 - Secuencias de comandos que se pueden ejecutar para automatizar tareas del proyecto.

Existen dos formas de crear nuestro `package.json`, la primera es de forma 
manual y la segunda es por medio del comando `npm init`. 

Si aún no sabe como crear un archivo `package.json`, puedes dar click 
[aquí](https://medium.com/noders/t%C3%BA-yo-y-package-json-9553929fb2e3). Te 
adjuntamos, además, la documentación oficial de `npm` acerca de 
[cómo crear este archivo](https://docs.npmjs.com/creating-a-package-json-file).

#### Observaciones
  1. Al crear nuestro `package.json` utilizando el comando `npm init` nos pedirá un 
    `entry point` o punto de entrada. Si nuestro proyecto fuera una librería, nuestro 
    `entry point` debería ser un archivo de extensión `.js`. En cambio, en un proyecto 
    web debería ser un archivo de extensión `.html`. Cabe recalcar que en éste último
    deberán cargarse los módulos de la lógica de nuestro proyecto. 
 
       - **entry point**: Archivo que incluirá la lógica principal de su módulo. Puede 
       ver más información acerca de este apartado 
       [aquí](https://stackoverflow.com/questions/32800066/what-is-entry-point-in-npm-init).

  2. En nuestro `package.json` encontraremos las siguientes estructuras:
   - `dependencies`: Aquí encontramos las dependencias de producción. Su uso es directo, 
   generalmente implementan parte del código. Ejemplo: Vue, React, Angular, Express, etc.
   - `devDependencies`:  Aquí encontramos las dependencias de desarrollo. Su uso se da en
   el proceso de compilación, herramientas que lo ayudan a administrar cómo terminará el 
   código final, módulos de prueba de terceros. Ejemplo: Jest, Mocha, Eslint, etc.

## Paso N°3:
Instalar la dependencia `serve` de `npm`. Este paquete nos va a permitir correr el 
servidor con el comando `npm start`.

Además, `serve` nos proporciona una interfaz ordenada que enumera los contenidos de
nuestro directorio.

Puede ver la documentación oficial de este paquete [aquí](https://www.npmjs.com/package/serve).


#### Observaciones:
 1. Diferencias al instalar paquetes:
     - `--save-dev`: Se utiliza para guardar el paquete con fines de desarrollo. Ejemplo: 
      pruebas unitarias, minificación.
     - `--save`: Se utiliza para guardar el paquete con fines de producción. Ejemplo:
      librerías o frameworks.

 2. Al instalar nuestra dependencia notaremos que se generan dos archivos de forma automática:
    - `node_modules`: Carpeta que almacena las módulos de nuestro proyecto. A medida que 
    instale más dependencias, el tamaño de esta carpeta aumentará rápidamente.
    - `package-lock.json`: Archivo que realiza un seguimiento de todos los cambios que se realizan 
    en package.json o node_modules y nos indica la versión exacta del paquete instalado. 
    
 3. Los archivos `node_modules` y `package-lock.json` se reconstruyen al ejecutar el comando 
    `npm install`. npm buscará un archivo package-lock.json para instalar los módulos. Si no
    hubiera ningún archivo de bloqueo disponible, leería el archivo package.json para determinar
    las instalaciones. En general, la instalación se puede realizar de manera más rápida desde 
    package-lock.json, ya que el archivo de bloqueo contiene la versión exacta de los módulos y 
    sus dependencias, lo cual significa que npm no tiene que invertir tiempo en determinar una 
    versión adecuada para la instalación.

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

