![](https://scontent.xx.fbcdn.net/hphotos-xfp1/v/t1.0-9/167359_123494254391056_5930879_n.jpg?oh=472b4c6e436ab91fd540c3f5ec6cf108&oe=57BB2020)
## Posada Piedras Anchas

> Una web applications, del tipo portal institucional, basado en Google Polymer 1.0, [Polimer Started Kit 1.0](https://developers.google.com/web/tools/polymer-starter-kit/)


### Incluye "out of the box":
* [Polymer](https://www.polymer-project.org/), [Paper](https://elements.polymer-project.org/browse?package=paper-elements), [Iron](https://elements.polymer-project.org/browse?package=iron-elements) elements
* [Material Design](http://www.google.com/design/spec/material-design/introduction.html) layout
* Routing with [Page.js](https://visionmedia.github.io/page.js)
* Unit testing with [Web Component Tester](https://github.com/Polymer/web-component-tester)
* End-to-end Build Tooling (including [Vulcanize](https://github.com/Polymer/vulcanize))


### Demo
> La última version demo (from master GitHub) se encuentra vulcanizada en [Piedras Anchas en FireBase.com](https://piedrasanchas.firebaseapp.com), basada en contenidos y estética de [Posada Piedras Anchas](http://www.posadapiedrasanchas.com.ar/)

Los datos son tomados con [FQL](https://developers.facebook.com/docs/reference/fql/) en formato [JSON](https://es.wikipedia.org/wiki/JSON) a traves del [Graph de Facebook](https://graph.facebook.com/fql), fotos y textos.

### Dependencias
* [Node.js](https://nodejs.org) a JavaScript runtime built on Chrome's V8 JavaScript engine & [npm](https://www.npmjs.com)
* [Gulp](http://gulpjs.com) the streaming build system
* [Bower](http://bower.io) A package manager for the web


#### Instalacion de las dependencias
En el root del directorio clonado de [GitHub](https://github.com/o00oooo/piedras-anchas), una vez instalado [Node.js](https://nodejs.org), abrir [Powershell](https://msdn.microsoft.com/en-us/powershell/) y correr:

```sh
npm install -g gulp bower && npm install && bower install
```


## Editor 
Archivos manipulados y editados con [Brackets](http://brackets.io/) con las siguientes extensiones:
* [Polymer Brackets Extension](https://github.com/chrisgriffith/Polymer-Brackets-Extension) los linter para Polymer
* [Emmet](http://emmet.io) abreviaciones para escribir html y css rapido
* [Brackets Color Highlighter](https://github.com/Taraflex/Brackets-Color-Highlighter) muestra los colores en los css dentro del paño del archivo
* [Brackets Gulp](https://github.com/ErezAlster/brackets-gulp) para arrancar el webserver local con debug
* [Brackets Icons](https://github.com/ivogabe/Brackets-Icons) muestra los archivos con los iconos standard de hoy
* [Brackets Git](https://github.com/zaggino/brackets-git) para manejar las ramificaciones dentro del brackets
* [Brackets Beautify](https://github.com/brackets-beautify/brackets-beautify) formatea el archivo al guardar
* [Brackets TODO](https://github.com/mikaeljorhult/brackets-todo) para traqueo de tareas y pendientes

Como alternativa todavia en face de pruebas se uso [VScode](https://code.visualstudio.com/)


## Deploy

### Github
Por supuesto usaremos [Git](https://github.com) para el control de versiones y ramificaciones.
El proyecto se aloja en [Piedras Anchas GH](https://github.com/o00oooo/piedras-anchas)


### Firebase
La aplicación release usa [Firebase](https://www.firebase.com/) para su publicación vulcanizada con gulp.
* [Webapp](https://piedrasanchas.firebaseapp.com/)
* [Gestión](https://piedrasanchas.firebaseio.com)

[Ver detalles en](https://www.polymer-project.org/1.0/docs/start/psk/deploy.html)




## Application Theming & Styling by Polymer SK

Polymer 1.0 introduces a shim for CSS custom properties. We take advantage of this in `app/styles/app-theme.html` to provide theming for your application. You can also find our presets for Material Design breakpoints in this file.

[Read more](https://www.polymer-project.org/1.0/docs/devguide/styling.html) about CSS custom properties.



## Frequently Asked Questions from PSK

### Where do I customise my application theme?

Theming can be achieved using [CSS Custom properties](https://www.polymer-project.org/1.0/docs/devguide/styling.html#xscope-styling-details) via [app/styles/app-theme.html](https://github.com/PolymerElements/polymer-starter-kit/blob/master/app/styles/app-theme.html).
You can also use `app/styles/main.css` for pure CSS stylesheets (e.g for global styles), however note that Custom properties will not work there under the shim.

A [Polycast](https://www.youtube.com/watch?v=omASiF85JzI) is also available that walks through theming using Polymer 1.0.

### Where do I configure routes in my application?

This can be done via [`app/elements/routing.html`](https://github.com/PolymerElements/polymer-starter-kit/blob/master/app/elements/routing.html). We use Page.js for routing and new routes
can be defined in this import. We then toggle which `<iron-pages>` page to display based on the [selected](https://github.com/PolymerElements/polymer-starter-kit/blob/master/app/index.html#L105) route.

### Why are we using Page.js rather than a declarative router like `<more-routing>`?

`<more-routing>` (in our opinion) is good, but lacks imperative hooks for getting full control
over the routing in your application. This is one place where a pure JS router shines. We may
at some point switch back to a declarative router when our hook requirements are tackled. That
said, it should be trivial to switch to `<more-routing>` or another declarative router in your
own local setup.

### Where can I find the application layouts from your Google I/O 2015 talk?

App layouts live in a separate repository called [app-layout-templates](https://github.com/PolymerElements/app-layout-templates).
You can select a template and copy over the relevant parts you would like to reuse to Polymer Starter Kit.

You will probably need to change paths to where your Iron and Paper dependencies can be found to get everything working.
This can be done by adding them to the [`elements.html`](https://github.com/PolymerElements/polymer-starter-kit/blob/master/app/elements/elements.html) import.
