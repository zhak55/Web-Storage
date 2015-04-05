# Intellectual Wars: based on Phaser Game Engine

# Features

- [Phaser][phaser] - game engine [Client]
- [jQuery][jquery] - dom [Client]
- [Browserify][browserify] - emulate require [Gulp/Sh]
- [EJS][ejs] - server templating [Server]
- [Sass][sass]: scss syntax* [Server/Local]
- [Compass][compass]: * [Server/Local]
- [MongoDB][mongo] - DB [Server]
- [Koala][koala]: In order to compile scss & compass locally [Local]
- [Mongoose][goose]: ODM for mongoDB [Server]
- [Express][express]: simplify work with node.js [Server]
- [Socket.io][socket]: real-time engine [Server & Client]
- [Gulp][gulp]: the streaming build system [Server]
- [ESLint][eslint]: keep your code clean [Server]
- [BrowserSync][browser-sync]: a local web server to test your code [Server]

_* Compass & Scss files can be compiled with Koala <br>
_*Uses separate states files and prefabs for the game objects, as
[Codevinsky][codevinsky] did in his great [tutorial][codevinsky-tutorial]. 

## Installation

Make sure [node][node], [gulp][gulp] and [slush][slush] are installed.

Then, install `slush-phaser-game` __globally__:

```sh
npm install -g slush-phaser-game
```

*Note: you may need to use sudo for this to work.*

## Usage

### Create a new project

Running the following command will create a new folder for your project:

```sh
slush phaser-game
```

You will be prompted to give your game a name, a resolution and the version of
Phaser you want to use.

### Get started

This will start the local web server and open your game in your browser:

```sh
gulp
```

Once the server is running, each modification will automatically update the page
opened in the browser.

A new folder (```build```) should appear at the root of your project, containing
the generated files (HTML, CSS and JS) for your game. That's the content of this
folder you'll use when publishing your game.

To list all the available options, you can use ```gulp -h```.

## The structure if IW

```
├── server                        # Here is located server logic 
├── assets                        # Assets folder: images are at the root...
|   ├── audio                     # ... audio and music files are here...
|   └── fonts                     # ... while fonts go there.
|   └── sprites
|   |   ├── json 
|   |   ├── sprites 
|   └── maps[backgrounds]
|   └── levels
|   └── ui
├── build                         # Generated folder.
|   ├── assets
|   ├── css
|   └── js
├── dist                          # Were you'll find the version you'll publish.
├── src
|   ├── scripts
|   |   ├── prefabs               # Put all your "prefabs" in that folder...
|   |   ├── states                # ... and your states in this one.
|   |   |   └── boot.js
|   |   |   └── menu.js
|   |   |   └── play.js
|   |   |   └── preloader.js
|   |   └── main.js               # Entry point of your code.
|   ├── stylesheets
|   |   └── style.styl
|   └── index.jade
├── tasks                         # Where the build tasks are. Each file in this
|   ├── build.js                  # directory will be called by gulp.
|   ├── clean.js
|   ├── default.js
|   ├── serve.js
|   └── watch.js
├── .bowerrc
├── .eslintrc
├── .gitignore
├── bower.json
├── config.js                     # A config file for your game.
├── gulpfile.js
└── package.json
```
---
[browser-sync]: http://www.browsersync.io/
[browserify]: http://browserify.org/
[codevinsky-tutorial]: http://www.codevinsky.com/phaser-2-0-tutorial-flappy-bird-part-1/
[eslint]: http://www.eslint.org/
[ejs]: http://www.embeddedjs.com/
[gulp]: http://gulpjs.com/
[node]: http://nodejs.org/
[phaser]: http://phaser.io/
[mongo]: https://www.mongodb.org/
[koala]: http://koala-app.com/
[goose]: http://mongoosejs.com/
[compass]: http://compass-style.org/
[express]: http://expressjs.com/
[socket]: http://socket.io/
[jquery]: https://jquery.com/
[sass]: http://sass-lang.com/
[gulp]: http://gulpjs.com/
[slush]: http://slushjs.github.io/
