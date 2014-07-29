#Node.js Starter Kit

> This repo is a starter kit for working with [Node.js](http://nodejs.org), [Handlebars](http://handlebarsjs.com) (both server and client side), [SASS](http://sass-lang.com) (through [Stylus](http://learnboost.github.io/stylus/)), and [RequireJS](http://requirejs.org). Client-side dependency management is through [Bower](http://bower.io). 

##Getting Started

Run the following command to download the repo and unpack it into `/nodejs-starter-kit-master`.

```bash
$ curl -L https://github.com/neogeek/nodejs-starter-kit/archive/master.tar.gz | tar -xz
```

All client-side files are located in `/static`. Bower components and compiled client-side Handlebars templates generated through `grunt` are also stored here.

Server-side Handlebars templates are stored in `/src/views`.

##Building

The following command will install all Node.js and Bower dependencies. Once all dependencies are installed it will run `grunt` compiling Handlebars and SASS files.

```bash
$ npm install
```

To manually compile Handlebars and SASS files run:

```bash
$ grunt
```

To watch for changes to any Handlebars or SASS files run:

```bash
$ grunt watch
```

##Testing

Tests are powered by [Jasmine](http://jasmine.github.io) and [PhantomJS](http://phantomjs.org). To run all tests use this command:

```bash
$ npm test
```

A `.travis.yml` configuration file is included to support automated testing through [Travis CI](https://travis-ci.org).

##Server

If you have the [Heroku Toolbelt](https://toolbelt.heroku.com) installed you can start the sample applications with this command:

```bash
$ foreman start
```

If not, then the application can also be run using this command:

```bash
$ node web.js
```

Once the application is running you can access it at <http://localhost:5000/>.

##Bash Alias

Add the following to your `~/.bash_profile` and restart terminal. You will now be able to create a new project using the starter kit by typing `nodejs-project test` (replacing _test_ with your new project name).

```bash
nodejs-project-builder() {

    curl -L https://github.com/neogeek/nodejs-starter-kit/archive/master.tar.gz | tar -xz
    mv nodejs-starter-kit-master $1
    cd $1
    npm install

}

alias nodejs-project=nodejs-project-builder
```
