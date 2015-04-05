# Intellectual Wars: based on Phaser Game Engine

# Features

- [Phaser][phaser]
- [Browserify][browserify]
- [EJS][ejs]
- [Stylus][stylus]
- [ESLint][eslint]: keep your code clean
- [BrowserSync][browser-sync]: a local web server to test your code

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
[stylus]: http://learnboost.github.io/stylus/
[slush]: http://slushjs.github.io/
