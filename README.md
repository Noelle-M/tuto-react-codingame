# tuto-react-codingame
## Ce tuto date de 2017 !
https://www.codingame.com/playgrounds/8894/redux-tutorial-for-beginners

#### Une fois le projet cloné, il faut lancer le commande :

<pre>npm install</pre>

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
<pre>npm install redux react-redux</pre>

Ainsi que le besoin de créer le dossier dist qui contient le fichier bundle.js

Pour résoudre l'erreur : "Uncaught SyntaxError: import declarations may only appear at top level of a module" : 
<pre>npm install --save-dev webpack webpack-cli webpack-dev-server babel-loader @babel/core @babel/preset-env @babel/preset-react
</pre>
L'erreur est due au fait que le navigateur ne prend pas en charge les importations de modules ES6 directement 
dans le fichier JavaScript sans utiliser un bundler tel que Webpack ou un compilateur comme Babel (oui déjà installer mais il manque l'essentiel).
Pour résoudre ce problème j'ai utilisé un bundler et un compilateur (recommandé) :
Je vous recommande d'utiliser un bundler comme Webpack et un compilateur comme Babel pour transpiler votre code en un format que 
les navigateurs peuvent comprendre.

#### Je ne suis pas sûre que 
<pre>babel-loader @babel/core @babel/preset-env @babel/preset-react</pre> 
soient nécessaire pour transpiler le code en JS (dans l'doute...).

et enfin :
<pre>npm install -g npm@latest</pre> 
Celle-ci est clairement de ma faute :p 

Tout ça est un chouilla le bazar, le tuto est vieux et GPT est un héro !
J'ai bien galéré et le projet ici est à jour ( pour le moment avril 2023 :p )
