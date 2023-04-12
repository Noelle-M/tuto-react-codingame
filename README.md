# tuto-react-codingame
## Ce tuto date de 2017 !
https://www.codingame.com/playgrounds/8894/redux-tutorial-for-beginners

### Créer un fichier package.json à la racine du projet.

{
    "name": "reduxapp",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
        "start": "webpack-dev-server"
    },
    "author": "KRUNAL LATHIYA",
    "license": "ISC",
    "devDependencies": {
        "babel-core": "^6.24.0",
        "babel-loader": "^6.4.1",
        "babel-preset-es2015": "^6.24.0",
        "babel-preset-react": "^6.23.0",
        "babel-preset-stage-3": "^6.22.0",
        "webpack": "^2.3.2",
        "webpack-dev-server": "^2.4.2"
    },
    "dependencies": {
        "react": "^15.4.2",
        "react-dom": "^15.4.2",
        "react-redux": "^5.0.6",
        "redux": "^3.7.2"
    }
}


----------------------------------------------------

### Switch to a terminal and type the following command.

npm install

---------------------------------------------------

### Créer un fichier webpack.config.js à la racine du projet

module.exports = {
    entry: './src/main.js',
    output: {
        filename: 'bundle.js'
    },
    module: {
        loaders: [
        {
            loader: 'babel-loader',
            test: /\.js$/,
            exclude: /node_modules/
        }
        ]
    },
    devServer: {
        port: 3000
    }
};


---------------------------------------------------

### Créer un fichier .babelrc à la racine du projet

{
  "presets": ["es2015", "react", "stage-3"]
}

---------------------------------------------------

Dans ce tuto CodinGame il n'est pas mentionné la commande :
<pre>npm install redux react-redux</pre>la création du dossier dist qui contient le fichier bundle.js

Pour résoudre l'erreur : "Uncaught SyntaxError: import declarations may only appear at top level of a module" : 
<pre>npm install --save-dev webpack webpack-cli webpack-dev-server babel-loader @babel/core @babel/preset-env @babel/preset-react
</pre>
L'erreur est due au fait que le navigateur ne prend pas en charge les importations de modules ES6 directement 
dans le fichier JavaScript sans utiliser un bundler tel que Webpack ou un compilateur comme Babel (oui déjà installer mais il manque l'essentiel).
Pour résoudre ce problème j'ai utilisé un bundler et un compilateur (recommandé) :
Je vous recommande d'utiliser un bundler comme Webpack et un compilateur comme Babel pour transpiler votre code en un format que 
les navigateurs peuvent comprendre.
<pre>npm install --save-dev webpack webpack-cli webpack-dev-server babel-loader @babel/core @babel/preset-env @babel/preset-react
</pre>

et enfin :
<pre>npm install -g npm@latest</pre> 
Celle-ci est clairement de ma faute :p 

Tout ça est un chouilla le bazar, le tuto est vieux et GPT est un héro !
J'ai bien galéré et le projet ici est à jour ( pour le moment avril 2023 :p )
