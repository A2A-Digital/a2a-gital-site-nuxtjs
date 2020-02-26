# Introduction
## What is Nuxt.js?

Nuxt is a progressive framework based on Vue.js to create modern web applications. It is based on Vue.js official libraries (vue, vue-router and vuex) and powerful development tools (webpack, Babel and PostCSS).

## What is NuxtJS?

NuxtJS is the backbone of your Vue.js project, giving structure to build your project with confidence while being flexible.

## Features

* Write Vue Files (*.vue)
* Automatic Code Splitting
* Server-Side Rendering
* Powerful Routing System with Asynchronous Data
* Static File Serving
* [ES2015+](https://babeljs.io/docs/en/learn/) Transpilation
* Bundling and minifying of your JS & CSS
* Hot module replacement in Development
* Pre-processor: Sass, Less, Stylus, etc.
* HTTP/2 push headers ready
* Extending with Modular architecture

## How it Works

Nuxt.js includes the following to create a rich web application development:
* [Vue 2](https://vuejs.org/)
* [Vue Router](https://router.vuejs.org/)
* [Vuex](https://vuex.vuejs.org/guide/)
* [Vue Server Render](https://ssr.vuejs.org/)
* [Vue Meta](https://github.com/nuxt/vue-meta)

## Schema

This schema shows what is called by Nuxt.js when the server is called or when the user navigates through the app via [nuxt-link](https://nuxtjs.org/api/components-nuxt-link/)

![Nuxt-link](/images/nuxt-schema.svg)

## Server Rendered (Universal SSR)

You can use Nuxt.js as a framework to handle all the UI rendering of your project.

When launching nuxt, it will start a development server with hot-reloading and [Vue Server Renderer](https://ssr.vuejs.org/) configured to automatically server-render your application.

# Getting Started
## Installation
Nuxt.js is really easy to get started with. A simple project only needs the nuxt dependency.
### Using create-nuxt-app
Make sure you have [npx](https://www.npmjs.com/package/npx) installed (npx is shipped by default since NPM 5.2.0)
```
$ npx create-nuxt-app <project-name>
```
Or with [yarn](https://classic.yarnpkg.com/en/):
```
    $ yarn create nuxt-app <project-name>
```
1. It will ask you some questions:
    * None (Nuxt default server)
    * [Express](https://github.com/expressjs/express)
    * [Koa](https://github.com/koajs/koa)
    * [Hapi](https://github.com/hapijs/hapi)
    * [Feathers](https://github.com/feathersjs/feathers)
    * [Micro](https://github.com/zeit/micro)
    * [Fastify](https://github.com/fastify/fastify)
    * [Adonis (WIP)](https://github.com/adonisjs/adonis-framework)
2. Choose your favorite UI framework:
    * None (feel free to add one later)
    * [Bootstrap](https://github.com/bootstrap-vue/bootstrap-vue)
    * [Vuetify](https://github.com/vuetifyjs/vuetify)
    * [Bulma](https://github.com/jgthms/bulma)
    * [Tailwind](https://github.com/tailwindcss/tailwindcss)
    * [Element UI](https://github.com/ElemeFE/element)
    * [Ant Design Vue](https://github.com/vueComponent/ant-design-vue)
    * [Buefy](https://github.com/buefy/buefy)
    * [iView](https://github.com/iview/iview)
    * [Tachyons](https://github.com/tachyons-css/tachyons)
3. Choose your favorite testing framework:
    * None (feel free to add one later)
    * [Jest](https://github.com/facebook/jest)
    * [AVA](https://github.com/avajs/ava)
4. The [Nuxt mode you want (Universal or SPA)](https://nuxtjs.org/guide#single-page-applications-spa-)
5. [Add axios module](https://github.com/nuxt-community/axios-module) to make HTTP request easily into your application.
6. Add [EsLint](https://eslint.org/) to Lint your  code on save.
7. Add [Prettier](https://prettier.io/) to prettify your code on save.
When answered, it will install all the dependencies so the next step is to navigate to the project folder and launch it with:
```
$ cd <project-name>
$ npm run dev
```
The application is now running on [http://localhost:3000](http://localhost:3000/).
```
Nuxt.js will listen for file changes inside the pages directory, so there is no need to restart the application when adding new pages.
```
To discover more about the directory structure of the project: [Directory Structure Documentation](https://nuxtjs.org/guide/directory-structure).

### Starting from scratch
Creating a Nuxt.js project from scratch is easy, `only 1 file and 1 directory are required`. Create an empty directory to start:

```
$ mkdir <project-name>
$ cd <project-name>
```
`Info`: replace `<project-name>` with a name for the project.

#### The package.json
Every project needs a `package.json` file to start `nuxt`. Copy this json into your package.json and save before running npm install (below):

```json
{
  "name": "my-app",
  "scripts": {
    "dev": "nuxt"
  }
}
```
`scripts` will launch Nuxt.js via `npm run dev`.

#### Installing `nuxt`
With the `package.json ` created, add `nuxt` to the project via npm:
```js
$ npm install --save nuxt
```
#### The `pages` directory
Nuxt.js transforms every `*.vue` file inside a `pages` directory as a route for the application.

Create the `pages` directory:

```bash
$ mkdir pages
```
then create the first page in `pages/index.vue:`
```html
<template>
  <h1>Hello world!</h1>
</template>
```
and launch the project with:
```
$ npm run dev
```
The application is now running on [http://localhost:3000](http://localhost:3000).
```
Nuxt.js will listen for file changes inside the pages directory, so there is no need to restart the application when adding new pages.
```
## Directory Structure
The default Nuxt.js application structure is intended to provide a great starting point for both small and large applications. Of course, you are free to organize your application however you like.
[Watch a free lesson](https://vueschool.io/lessons/guided-nuxtjs-project-tour?friend=nuxt) about the Nuxt.js directory structure on Vue School
### Directories
#### The Assets Directory
The `assets` directory contains your un-compiled assets such as Stylus or Sass files, images, or fonts.

[More documentation about Assets integration](https://nuxtjs.org/guide/assets)
##### The Components Directory
The `components` directory contains your Vue.js Components. You can't use either `asyncData` or `fetch` in these components.
##### The Layouts Directory
The `layouts` directory includes your application layouts. Layouts are used to change the look and feel of your page (for example by including a sidebar).

[More documentation about Layouts integration](https://nuxtjs.org/guide/views#layouts)

This directory cannot be renamed without extra configuration.
##### The Middleware Directory
The `middleware` directory contains your Application Middleware. Middleware lets you define custom functions that can be run before rendering either a page or a group of pages (layouts).
[The Middleware Directory](https://nuxtjs.org/guide/routing#middleware)
##### The Pages Directory
The `pages` directory contains your Application Views and Routes. The framework reads all the `.vue` files inside this directory and creates the application router.

This directory cannot be renamed without extra configuration.

[More documentation about Pages integration](https://nuxtjs.org/guide/views)
##### The Plugins Directory
The `plugins` directory contains your Javascript plugins that you want to run before instantiating the root Vue.js Application. This is the place to register components globally and to inject functions or constants.

[More documentation about Plugins integration](https://nuxtjs.org/guide/plugins)
##### The Static Directory
The `static` directory is directly mapped to the server root `(/static/robots.txt` is accessible under `http://localhost:3000/robots.txt`) and contains files that likely won't be changed (e.g. the favicon)

Example: `/static/robots.txt` is mapped as `/robots.txt`

This directory cannot be renamed without extra configuration.

[More documentation about Static integration](https://nuxtjs.org/guide/assets#static)
##### The Store Directory
The `store` directory contains your [Vuex Store](https://vuex.vuejs.org/guide/) files. The Vuex Store comes with Nuxt.js out of the box but is disabled by default. Creating an `index.js` file in this directory enables the store.

This directory cannot be renamed without extra configuration.

[More documentation about Store integration](https://nuxtjs.org/guide/configuration)

##### The nuxt.config.js File
The `nuxt.config.js` file contains your Nuxt.js custom configuration.

This file cannot be renamed without extra configuration.

[More documentation about nuxt.config.js integration](https://nuxtjs.org/guide/configuration)
##### The package.json File
The `package.json` file contains your Application dependencies and scripts.

`This file cannot be renamed`.
## Configuration

By default, `Nuxt.js` is configured to cover most use cases. This default configuration can be overwritten with the nuxt.config.js file.
### build
This option lets you configure various settings for the `build` step, including `loaders`, `filenames`, the `webpack` config and transpilation.

[Documentation about build integration](https://nuxtjs.org/api/configuration-build)
### css
This option lets you define the CSS files, modules, and libraries you want to include globally (on every page).

[Documentation about css integration](https://nuxtjs.org/api/configuration-css)
### dev
This option lets you define the `development` or `production` mode of Nuxt.js (important when you use Nuxt.js programatically)

[pocumentation about dev integration](https://nuxtjs.org/api/configuration-dev)
### env
This option lets you define environment variables that are available to both client and server.
[Documentation about env integration](https://nuxtjs.org/api/configuration-env)
### generate
This option lets you set up parameter values for every dynamic route in your application that will be transformed into HTML files by Nuxt.js.

[Documentation about generate integration](https://nuxtjs.org/api/configuration-generate)
### head
This option lets you define all default meta tags for your application.

[Documentation about head integration](https://nuxtjs.org/api/configuration-head)
### loading
This option lets you customize the loading component that Nuxt.js uses by default.

[Documentation about loading integration](https://nuxtjs.org/api/configuration-loading)

### modules
With this option you can add Nuxt.js modules to your project.

[Documentation about modules integration](https://nuxtjs.org/api/configuration-modules)

### modulesDir
This option lets you define the node_modules folder of your Nuxt.js Application.

[Documentation about modulesDir integration](https://nuxtjs.org/api/configuration-plugins)

### plugins
This option lets you define JavaScript plugins that should be run before instantiating the root Vue.js application.

[Documentation about plugins integration](https://nuxtjs.org/api/configuration-plugins)
 ### rootDir
 This option lets you define the workspace of your Nuxt.js application.

 [Documentation about rootDir integration](https://nuxtjs.org/api/configuration-rootdir)

 ### router
 With the router option you overwrite the default Nuxt.js configuration of Vue Router.

[Documentation about router integration](https://nuxtjs.org/api/configuration-router)
### server
This option lets you configure the connection variables for the server instance of your Nuxt.js application.

[Documentation about server integration](https://nuxtjs.org/api/configuration-server)
### srcDir
This option lets you define the source directory of your Nuxt.js application.

[Documentation about srcDir integration](https://nuxtjs.org/api/configuration-srcdir)
### dir
This option lets you define the custom directories of your Nuxt.js application.

[Documentation about dir integration](https://nuxtjs.org/api/configuration-dir)
### transition
This option lets you define the default properties of the page transitions.

[Documentation about transition integration](https://nuxtjs.org/api/configuration-transition)
### Asynchronous Configuration
If you need to populate some options (e.g. the head) with asynchronous data (e.g. coming from an API), you have the possibility to return a promise. Here is an example:
```js
/* 
axios-module cannot be used in nuxt.config.js
You need to import axios and configure it again
*/
import axios from 'axios'

export default async () => {
  const data = await axios.get('endpoint')
  return {
    head: {
      title: data.head.title,
      //... rest of config
    }
  }
}
```
## Routing
Nuxt.js automatically generates the [vue-router](https://github.com/vuejs/vue-router) configuration based on your file tree of Vue files inside the `pages` directory.
To navigate between pages, we recommend to use the `<nuxt-link>` component.
For example:
```html
<template>
  <nuxt-link to="/">Home page</nuxt-link>
</template>
```
### Basic Routes
This file tree:
```
pages/
--| user/
-----| index.vue
-----| one.vue
--| index.vue
```
will automatically generate:
```js
router: {
  routes: [
    {
      name: 'index',
      path: '/',
      component: 'pages/index.vue'
    },
    {
      name: 'user',
      path: '/user',
      component: 'pages/user/index.vue'
    },
    {
      name: 'user-one',
      path: '/user/one',
      component: 'pages/user/one.vue'
    }
  ]
}
```
### Dynamic Routes
To define a dynamic route with a parameter, you need to define a .vue file OR a directory  `prefixed by an underscore`.

[Watch a free lesson about](https://vueschool.io/lessons/nuxtjs-dynamic-routes?friend=nuxt) `dynamic routes` on Vue School

This file tree:
```
pages/
--| _slug/
-----| comments.vue
-----| index.vue
--| users/
-----| _id.vue
--| index.vue
```
will automatically generate:
```js
router: {
  routes: [
    {
      name: 'index',
      path: '/',
      component: 'pages/index.vue'
    },
    {
      name: 'users-id',
      path: '/users/:id?',
      component: 'pages/users/_id.vue'
    },
    {
      name: 'slug',
      path: '/:slug',
      component: 'pages/_slug/index.vue'
    },
    {
      name: 'slug-comments',
      path: '/:slug/comments',
      component: 'pages/_slug/comments.vue'
    }
  ]
}
```
As you can see the route named `users-id` has the path `:id?` which makes it optional, if you want to make it required, create an `index.vue` file in the `users/_id` directory instead.
```
Warning: dynamic routes are ignored by the generate command: API Configuration generate
```
### Validate Route Params
Nuxt.js lets you define a validator method inside your dynamic route component.

In this example: `pages/users/_id.vue`
```js
export default {
  validate ({ params }) {
    // Must be a number
    return /^\d+$/.test(params.id)
  }
}
```
If the validate method does not return `true` or a `Promise` that resolve to true, or throws an Error, Nuxt.js will automatically load the 404 error page or 500 error page in case of an error.

More information about the validate method: [API Pages validate](https://nuxtjs.org/api/pages-validate)

### Nested Routes
Nuxt.js lets you create nested route by using the children routes of `vue-router`.

To define the parent component of a nested route, you need to create a Vue file with the `same name as the directory` which contain your children views.

Warning: don't forget to include `<nuxt-child/>` inside the parent component (`.vue` file).
This file tree:
```bash
pages/
--| users/
-----| _id.vue
-----| index.vue
--| users.vue
```
will automatically generate:
```js
router: {
  routes: [
    {
      path: '/users',
      component: 'pages/users.vue',
      children: [
        {
          path: '',
          component: 'pages/users/index.vue',
          name: 'users'
        },
        {
          path: ':id',
          component: 'pages/users/_id.vue',
          name: 'users-id'
        }
      ]
    }
  ]
}
```
### Dynamic Nested Routes
This scenario should not often happen, but it is possible with Nuxt.js: having dynamic children inside dynamic parents.

This file tree:
```bash
pages/
--| _category/
-----| _subCategory/
--------| _id.vue
--------| index.vue
-----| _subCategory.vue
-----| index.vue
--| _category.vue
--| index.vue
```
will automatically generate:
```js
router: {
  routes: [
    {
      path: '/',
      component: 'pages/index.vue',
      name: 'index'
    },
    {
      path: '/:category',
      component: 'pages/_category.vue',
      children: [
        {
          path: '',
          component: 'pages/_category/index.vue',
          name: 'category'
        },
        {
          path: ':subCategory',
          component: 'pages/_category/_subCategory.vue',
          children: [
            {
              path: '',
              component: 'pages/_category/_subCategory/index.vue',
              name: 'category-subCategory'
            },
            {
              path: ':id',
              component: 'pages/_category/_subCategory/_id.vue',
              name: 'category-subCategory-id'
            }
          ]
        }
      ]
    }
  ]
}
```
### Unknown Dynamic Nested Routes
If you do not know the depth of your URL structure, you can use `_.vue` to dynamically match nested paths. This will handle requests that do not match a more specific request.

This file tree:
```bash
pages/
--| people/
-----| _id.vue
-----| index.vue
--| _.vue
--| index.vue
```
Will handle requests like this:

```bash
Path	                            File
/	                                index.vue
/people	                            people/index.vue
/people/123	                        people/_id.vue
/about	                            _.vue
/about/careers  	                _.vue
/about/careers/chicago	            _.vue
```
Note: Handling `404 pages` is now up to the logic of the `_.vue page`. [More on 404 redirecting can be found here](https://nuxtjs.org/guide/async-data#handling-errors).

### Named Views
To render named views you can use `<nuxt name="top"/>` or `<nuxt-child name="top"/>` components in your `layout/page`. To specify named view of page we need to extend router config in nuxt.config.js file:

```js
export default {
  router: {
    extendRoutes (routes, resolve) {
      const index = routes.findIndex(route => route.name === 'main')
      routes[index] = {
        ...routes[index],
        components: {
          default: routes[index].component,
          top: resolve(__dirname, 'components/mainTop.vue')
        },
        chunkNames: {
          top: 'components/mainTop'
        }
      }
    }
  }
}
```
It require to extend interested route with 2 properties `components` and `chunkNames`. Named view in this config example has name `top`.

To see an example, take a look at the [named-views example](https://nuxtjs.org/examples/named-views).

### SPA fallback
You can enable `SPA` fallbacks for dynamic routes too. Nuxt.js will output an extra file that is the same as the `index.html` that would be used in `mode: 'spa'`. Most static hosting services can be configured to use the SPA template if no file matches. It won't include the `head` info or any HTML, but it will still resolve and load the data from the API.

We enable this in our `nuxt.config.js` file:

```js
export default {
  generate: {
    fallback: true, // if you want to use '404.html' instead of the default '200.html'
    fallback: 'my-fallback/file.html' // if your hosting needs a custom location
  }
}
```
### Locally Accessing Route Params
You can access the current route parameters within your local page or component by referencing `this.$route.params.{parameterName}`. For example, if you had a dynamic users page `(users\_id.vue)` and wanted to access the `id` parameter to load the user or process information, you could access the variable like `this`: `this.$route.params.id`.

Implementation for Surge
Surge [can handle](https://surge.sh/help/adding-a-custom-404-not-found-page) both `200.html` and `404.html`. `generate.fallback` is set to `200.html` by default, so no need to change it.

Implementation for GitHub Pages and Netlify
GitHub Pages and Netlify recognize the `404.html` file automatically, so setting `generate.fallback` to `true` is all we have to do!

Implementation for Firebase Hosting
Firebase Hosting [can handle](https://firebase.google.com/docs/hosting/full-config#404) the `404.html` file automatically, so setting `generate.fallback` to `true` will render the error page with a default response code of 404.
### Transitions
Nuxt.js uses the `<transition>` component to let you create amazing transitions/animations between your routes.

### Global Settings
```bash
Info: Nuxt.js default transition name is "page".
```

To add a fade transition to every page of your application, we need a CSS file that is shared across all our routes, so we start by creating a file in the assets folder.

Our global css in `assets/main.css`:
```css
.page-enter-active, .page-leave-active {
  transition: opacity .5s;
}
.page-enter, .page-leave-to {
  opacity: 0;
}
```
Then we add its path to the `css` array in our `nuxt.config.js` file:
```js
export default {
  css: [
    '~/assets/main.css'
  ]
}
```
More information about the transition key: [API Configuration transition](https://nuxtjs.org/api/pages-transition)
### Page Settings
You can also define a custom `transition` for a specific page with the transition property.

We add a new class in our global css in `assets/main.css`:
```css
.test-enter-active, .test-leave-active {
  transition: opacity .5s;
}
.test-enter, .test-leave-active {
  opacity: 0;
}
```
Then we use the transition property to define the class name to use for this page transition:
```js
export default {
  transition: 'test'
}
```
More information about the transition property: [API Pages transition](https://nuxtjs.org/api/pages-transition)
### Middleware
```css
Middleware lets you define custom functions that can be run before rendering either a page or a group of pages.
```

`Shared middleware should be placed in the middleware/ directory`. The filename will be the name of the middleware (`middleware/auth.js` will be the `auth` middleware). You can also defined page-specific middleware by using a function directly, see [anonymous middleware](https://nuxtjs.org/api/pages-middleware#anonymous-middleware).

A middleware receives the [context](https://nuxtjs.org/api/context) as first argument:
```js
export default function (context) {
  context.userAgent = process.server ? context.req.headers['user-agent'] : navigator.userAgent
}
```
In universal mode, middlewares will be called server-side once (on the first request to the Nuxt app or when page refreshes) and client-side when navigating to further routes. In SPA mode, middlewares will be called client-side on the first request and when navigating to further routes.

The middleware will be executed in series in this order:
1. `nuxt.config.js` (in the order within the file)
2. Matched layouts
3. Matched pages
A middleware can be asynchronous. To do this, simply return a `Promise` or use the 2nd `callback` argument:

`middleware/stats.js`
```js
import axios from 'axios'

export default function ({ route }) {
  return axios.post('http://my-stats-api.com', {
    url: route.fullPath
  })
}
```

Then, in your `nuxt.config.js`, use the `router.middleware` key:

`nuxt.config.js`
```js
export default {
  router: {
    middleware: 'stats'
  }
}
```
Now the `stats` middleware will be called for every route change.

You can add your middleware (even multiple) to a specific layout or page as well:

`pages/index.vue` or `layouts/default.vue`
```js
export default {
  middleware: ['auth', 'stats']
}
```
To see a real-life example using the middleware, please see [example-auth0](https://github.com/nuxt/example-auth0) on GitHub.
## Views
The Views section describes all you need to configure data and views for a specific route in your Nuxt.js Application `(App Template, Layouts, Pages and HTML Head)`.

![Views](/images/nuxt-views-schema.svg)

### App Template
You can customize the HTML app template used by Nuxt.js to include scripts or conditional CSS classes.

To change the template, create an `app.html` file, in the src folder of your project. (which is the project's root directory by default).

The default template used by `Nuxt.js` is:
```html
<!DOCTYPE html>
<html {{ HTML_ATTRS }}>
  <head {{ HEAD_ATTRS }}>
    {{ HEAD }}
  </head>
  <body {{ BODY_ATTRS }}>
    {{ APP }}
  </body>
</html>
```
One use case of using a custom app template is to add conditional CSS classes for IE:
```html
<!DOCTYPE html>
<!--[if IE 9]><html lang="en-US" class="lt-ie9 ie9" {{ HTML_ATTRS }}><![endif]-->
<!--[if (gt IE 9)|!(IE)]><!--><html {{ HTML_ATTRS }}><!--<![endif]-->
  <head {{ HEAD_ATTRS }}>
    {{ HEAD }}
  </head>
  <body {{ BODY_ATTRS }}>
    {{ APP }}
  </body>
</html>
```
### Layouts
Layouts are a great help when you want to change the look and feel of your Nuxt.js app. Whether you want to include a sidebar or having distinct layouts for mobile and desktop
### Default Layout
You can extend the main layout by adding a `layouts/default.vue` file. It will be used for all pages that don't have a layout specified.
```html
Info: Make sure to add the <nuxt/> component when creating a layout to actually include the page component.
```
The default layout that comes out of the box is just three lines long and simply renders the page component:
```html
<template>
  <nuxt/>
</template>
```
### Custom Layout
Every file (top-level) in the `layouts` directory will create a custom `layout` accessible with the layout property in the page components.

Let's say we want to create a blog layout and save it to `layouts/blog.vue`:
```html
<template>
  <div>
    <div>My blog navigation bar here</div>
    <nuxt/>
  </div>
</template>
```
Then we have to tell the pages (i.e. `pages/posts.vue`) to use your custom layout:
```html
<template>
<!-- Your template -->
</template>
<script>
export default {
  layout: 'blog'
  // page component definitions
}
</script>
```
More information about the `layout` property: [API Pages layout](https://nuxtjs.org/api/pages-layout)

Check out the [demonstration video](https://www.youtube.com/watch?v=YOKnSTp7d38) to see custom layouts in action.
### Error Page
The error page is a page component which is always displayed when an error occurs (that does not happen while server-side rendering).
```css
Warning: Though this file is placed in the layouts folder, it should be treated as a page.
```
As mentioned above, this layout is special, since you `should not` include `<nuxt/>` inside its template. You must see this layout as a component displayed when an error occurs (`404`, `500`, etc.). Similar to other page components, you can set a custom layout for the error page as well in the usual way.

The default error page source code is [available on GitHub](https://github.com/nuxt/nuxt.js/blob/dev/packages/vue-app/template/components/nuxt-error.vue).

You can customize the error page by adding a `layouts/error.vue` file:
```html
<template>
  <div class="container">
    <h1 v-if="error.statusCode === 404">Page not found</h1>
    <h1 v-else>An error occurred</h1>
    <nuxt-link to="/">Home page</nuxt-link>
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'blog' // you can set a custom layout for the error page
}
</script>
```
### Pages
Every Page component is a Vue component but Nuxt.js adds special attributes and functions to make the development of your universal application as easy as possible.

[Watch a free lesson about ``Nuxt.js Page Components`` on Vue School](https://vueschool.io/lessons/nuxtjs-page-components?friend=nuxt)
```html
<template>
  <h1 class="red">Hello {{ name }}!</h1>
</template>

<script>
export default {
  asyncData (context) {
    // called every time before loading the component
    // as the name said, it can be async
    // Also, the returned object will be merged with your data object
    return { name: 'World' }
  },
  fetch () {
    // The `fetch` method is used to fill the store before rendering the page
  },
  head () {
    // Set Meta Tags for this Page
  },
  // and more functionality to discover
  ...
}
</script>

<style>
.red {
  color: red;
}
</style>
```
![pageDetails](/images/view.PNG)
### HTML Head

Nuxt.js uses [vue-meta](https://vue-meta.nuxtjs.org/) to update the `document head` and `meta attributes` of your application.

The `vue-meta` Nuxt.js uses can be [found on GitHub](https://github.com/nuxt/nuxt.js/blob/dev/packages/vue-app/template/index.js#L42-L48).
```bash
Info: Nuxt.js uses hid instead of the default vmid key to identify meta elements
```
### Default Meta Tags
Nuxt.js lets you define all default `<meta>` tags for your application inside `nuxt.config.js`. Define them using the same `head` property:
Example of a custom viewport with a custom Google font:
```js
head: {
  meta: [
    { charset: 'utf-8' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Roboto' }
  ]
}
```
To learn more about the options available for `head`, take a look at [vue-meta documentation](https://vue-meta.nuxtjs.org/api/#metainfo-properties).

More information about the `head` method are available on the [API Configuration head](https://nuxtjs.org/api/configuration-head) page.
## Async Data
You may want to fetch data and render it on the server-side. Nuxt.js adds an `asyncData` method to let you handle async operations before initializing the component.
### The asyncData method
Sometimes you just want to fetch data and pre-render it on the server without using a store. `asyncData` is called every time before loading the `page` component. It will be called server-side once (on the first request to the Nuxt app) and client-side when navigating to further routes. This method receives the [context](https://nuxtjs.org/api/context) as the first argument, you can use it to fetch some data and Nuxt.js will merge it with the component data.

Nuxt.js will automatically merge the returned object with the component data.
```bash
You do NOT have access of the component instance through this inside asyncData because it is called before initiating the component.

```
Nuxt.js offers you different ways to use `asyncData`. Choose the one you're the most familiar with:
1. Returning a `Promise`. Nuxt.js will wait for the promise to be resolved before rendering the component.
2. Using the [async/await (learn more about it)](https://zeit.co/blog/async-and-await)

We are using [axios](https://github.com/axios/axios) to make isomorphic HTTP requests, we `strongly recommend` to use our [axios module](https://axios.nuxtjs.org/) for your Nuxt projects.

If you are using `axios` directly from `node_modules` and used the `axios.interceptors` to add interceptors to transform the data, make sure to create an instance before adding interceptors. If not, when you refresh the serverRender page, the interceptors will be added multiple times, which will cause a data error.
```js
import axios from 'axios'
const myaxios = axios.create({
  // ...
})
myaxios.interceptors.response.use(function (response) {
  return response.data
}, function (error) {
  // ...
})
```
### Returning a Promise
```js
export default {
  asyncData ({ params }) {
    return axios.get(`https://my-api/posts/${params.id}`)
      .then((res) => {  
  }
}
```
### Using async/await
```js
export default {
  async asyncData ({ params }) {
    const { data } = await axios.get(`https://my-api/posts/${params.id}`)
    return { title: data.title }
  }
}

```
### Displaying the data
The result from asyncData will be `merged` with data. You can display the data inside your template like you're used to doing:
```html
<template>
  <h1>{{ title }}</h1>
</template>
```
### The Context
To see the list of available keys in `context`, take a look at the [API Essential context](https://nuxtjs.org/api/context).
### Use `req/res` objects
When `asyncData` is called on server side, you have access to the `req` and `res` objects of the user request.
```js
export default {
  async asyncData ({ req, res }) {
    // Please check if you are on the server side before
    // using req and res
    if (process.server) {
      return { host: req.headers.host }
    }

    return {}
  }
}
```
### Accessing dynamic route data

You can use the `context` parameter to access dynamic route data as well! For example, dynamic route params can be retrieved using the name of the file or folder that configured it. If you've defined a file named `_slug.vue` in your `pages` folder, you can access the value via `context.params.slug`:
```js
export default {
  async asyncData ({ params }) {
    const slug = params.slug // When calling /abc the slug will be "abc"
    return { slug }
  }
}
```
### Listening to query changes
The `asyncData` method is not called on query string changes by default. If you want to change this behavior, for example when building a pagination component, you can set up parameters that should be listened to with the `watchQuery` property of your page component. Learn more on the [API watchQuery page](https://nuxtjs.org/api/pages-watchquery) page.

### Handling Errors
Nuxt.js adds the `error(params)` method in the `context`, which you can call to display the error page. `params.statusCode` will be also used to render the proper status code from the server-side.

Example with a `Promise`:

```js
export default {
  asyncData ({ params, error }) {
    return axios.get(`https://my-api/posts/${params.id}`)
      .then((res) => {
        return { title: res.data.title }
      })
      .catch((e) => {
        error({ statusCode: 404, message: 'Post not found' })
      })
  }
}
```
## Assets
By default, Nuxt uses vue-loader, file-loader and url-loader webpack loaders for strong assets serving. You can also use the `static` directory for static assets.
### Webpack
[vue-loader](https://vue-loader.vuejs.org/) automatically processes your style and template files with `css-loader` and the Vue template compiler out of the box. In this compilation process, all asset URLs such as `<img src="...">, background: url(...)` and `CSS @import` are resolved as module dependencies.

For example, we have this file tree:
```bash
-| assets/
----| image.png
-| pages/
----| index.vue
```
If you use `url('~assets/image.png')` in your CSS, it will be translated into `require('~/assets/image.png')`.
```
Warning: Starting from Nuxt 2.0 the ~/ alias won't be resolved correctly in your CSS files. You must use ~assets (without a slash) or the @ alias in url CSS references, i.e. background: url("~assets/banner.svg")
```
Or if you reference that image in your `pages/index.vue`:
```html
<template>
  <img src="~/assets/image.png">
</template>
```
It will be compiled into:
```js
createElement('img', { attrs: { src: require('~/assets/image.png') } })
```
Because `.png` is not a JavaScript file, Nuxt.js configures webpack to use [file-loader](https://github.com/webpack-contrib/file-loader) and [url-loader](https://github.com/webpack-contrib/url-loader) to handle them for you.

The benefits of these loaders are:
* `file-loader` lets you designate where to copy and place the asset file, and how to name it using version hashes for better caching. In production, you will benefit from long-term caching by default!
* `url-loader` allows you to conditionally inline a file as base-64 data URL if they are smaller than a given threshold. This can reduce a number of HTTP requests for trivial files. If the file is larger than the threshold, it automatically falls back to file-loader.

For those two loaders, the default configuration is:
```js
// https://github.com/nuxt/nuxt.js/blob/dev/packages/webpack/src/config/base.js#L297-L316
[
  {
    test: /\.(png|jpe?g|gif|svg|webp)$/,
    loader: 'url-loader',
    query: {
      limit: 1000, // 1kB
      name: 'img/[name].[hash:7].[ext]'
    }
  },
  {
    test: /\.(woff2?|eot|ttf|otf)(\?.*)?$/,
    loader: 'url-loader',
    query: {
      limit: 1000, // 1kB
      name: 'fonts/[name].[hash:7].[ext]'
    }
  }
]
```
Which means that every file below 1 KB will be inlined as base-64 data URL. Otherwise, the image/font will be copied in its corresponding folder (under the `.nuxt` directory) with a name containing a version hash for better caching.

When launching our application with `nuxt`, our template in `pages/index.vue`:
```html
<template>
  <img src="~/assets/image.png">
</template>
```
Will be transformed into:
```html
<img src="/_nuxt/img/image.0c61159.png">
```
If you want to change the loader configurations, please use [build.extend](https://nuxtjs.org/api/configuration-build#extend).
### Static
If you don't want to use Webpack assets from the `assets` directory, you can create and use the `static` directory (in your project root folder).

All included files will be automatically served by Nuxt and are accessible through your project root URL. (`static/favicon.ico` will be available at `localhost:3000/favicon.ico`)

This option is helpful for files like `robots.txt`, `sitemap.xml` or `CNAME` (which is important for GitHub Pages deployment).

In your code, you can then reference these files relative to the root (`/`):
```html
<!-- Static image from static directory -->
<img src="/my-image.png"/>

<!-- webpacked image from assets directory -->
<img src="~/assets/my-image-2.png"/>
```