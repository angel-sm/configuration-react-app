# Configurar React app
* **librerias**
	* babel
	* webpack
	* eslint

#### iniciar nuestro proyecto
	$ npm i -y
 
#### agregar React

	$ npm i --save react react-dom
   
#### agregar babel
> usamos babel para la compatibiladad con todos los navegadores

	$ npm install --save-dev @babel/core @babel/preset-env @babel/preset-react babel-loader

#### configuracion babel
> creamos el archivo .babelrc en la raiz del proyecto y pegamos la siguiente configuracion
	
    {
  	  "presets": [
    	  "@babel/preset-env",
    	  "@babel/preset-react"
  	  ],
    }

#### agregar webpack
	$ npm i -D webpack webpack-cli html-webpack-plugin html-loader
 
#### configurar webpack
> creamos nuestro archivo webpack.config.js en la raiz del proyecto para configurar webpack
*[webpack.config.js](https://gist.github.com/pachecodesm/5588a515592988094f718a1b44a42d58)*

#### comando build
> configuramos nuestro comando build dentro de nuestro archivo package.json

	{
  	"scripts": {
    	"build": "webpack --mode production"
  	},
	}
    
#### configurar webpack como entorno de desarrollo
> agregamos webpack-dev-serve para crear nuestro entorno de desarrollo y tener cambios en tiempo real

	$ npm install --save-dev webpack-dev-server

#### comando dev
> creamos nuestro comando para correr nuestro entorno de desarrollo
	
    {
  	  "scripts": {
    	  "start": "webpack-dev-server --open --mode development"
  	  },
	}


#### agregar ESLint
	$ npm i -D eslint babel-eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-react eslint-plugin-jsx-a11y
	
#### configrar ESLint
> cramos nuestro archivo .eslintrc en la raiz de nuestro proyecto y agregamos la configuracion de airbnb 
*[.eslintrc](https://gist.github.com/pachecodesm/b2d47a03b6541080838606a500bd257e)*

