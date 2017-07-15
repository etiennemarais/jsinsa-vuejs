# Journey into VueJS - JSINSA 2017 

## Official Resources

- [VueJS](https://vuejs.org/v2/guide/)
- [Vue Router](https://router.vuejs.org/en/)
- [Vuex](https://vuex.vuejs.org/en/)
- [Vue Server side rendering](https://vuejs.org/v2/guide/ssr.html)
- [Hackernews clone example app](https://github.com/vuejs/vue-hackernews-2.0)


## Community Resources

- An awesome curated [list](https://github.com/vuejs/awesome-vue) of vue resources exists on github.
- [Curated list of vue components](https://curated.vuejs.org/)
- [Learn Vue 2 step by step on laracasts](https://laracasts.com/series/learn-vue-2-step-by-step/episodes/19)
- [Laravel/VueJS App example with JWT](https://github.com/phanan/koel)
- [Intro into VueJS, Originally by Sarah Drasner (https://github.com/sdras)](https://github.com/sdras/intro-to-vue)

## Webpack and Laravel mix

[Laravel mix](https://github.com/JeffreyWay/laravel-mix) and [More docs](https://laravel.com/docs/5.4/mix) aims to simplify the webpack configuration for code loading if you are using `.vue` files. This will automatically split up your html/css and javascript bvy using [vue-loader](https://github.com/vuejs/vue-loader) under the hood.

```js
let mix = require('laravel-mix');

mix.js('resources/assets/js/main.js', 'public/js')
    .copy('node_modules/font-awesome/fonts', 'public/fonts')
    .sass('resources/assets/sass/app.scss', 'public/css')
    .version();
```

#### Package.json

Below is a typical package.json of a vuejs app. We need the babel2015 preset to make the javascript loader spit out browser compatible scripts.

```json
{
    "private": true,
    "scripts": {
        "dev": "node node_modules/cross-env/dist/bin/cross-env.js NODE_ENV=development node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
        "watch": "node node_modules/cross-env/dist/bin/cross-env.js NODE_ENV=development node_modules/webpack/bin/webpack.js --watch --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
        "production": "node node_modules/cross-env/dist/bin/cross-env.js NODE_ENV=production node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js"
    },
    "devDependencies": {
        "babel-preset-es2015": "^6.24.1",
        "babel-register": "^6.22.0",
        "browser-env": "^2.0.21",
        "cross-env": "^5.0.1",
        "font-awesome": "^4.7",
        "laravel-mix": "^0.12",
        "vue": "^2.3"
    },
    "babel": {
        "presets": [
            "es2015"
        ]
    }
}
```


