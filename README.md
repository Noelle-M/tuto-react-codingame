# tuto-react-codingame
## Ce tuto date de 2017 !

Create one project folder and in that create one file called package.json. Copy the following code into it.

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

Switch to a terminal and type the following command.

npm install

---------------------------------------------------

Next step will be to create the webpack.config.js file in the root folder.

// webpack.config.js

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

Also, create one file called in root called .babelrc

{
  "presets": ["es2015", "react", "stage-3"]
}
