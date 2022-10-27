# Pasos para la instalacion de NPM

## 1. Inicializar NPM

```sh
cd ir/hasta/tu/proyecto
npm init
```
continuar el proceso hasta el final con los valores por default.


## 2. Instalar node-ssas y nodemon

```sh
npm install -D node-sass nodemon
```

## 3. Creación de archivos de SCSS (Sass)

Agregar archivos de SCSS

## 4. Creación de nuevos comandos para compilar

En el package.json reemplazar las lineas de script:
```json
 "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```

 por lo siguiente:
 ```json
  "scripts": {
    "build-css": "node-sass --include-path scss scss/main.scss estilos/style.css",
    "watch-css": "nodemon -e scss -x \"npm run build-css\""
  },
```

## 5. Ejecutar el comando para compilar

```sh
npm run build-css
```
