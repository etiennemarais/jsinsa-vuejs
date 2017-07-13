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
- [Laravel mix](https://github.com/JeffreyWay/laravel-mix) and [More docs](https://laravel.com/docs/5.4/mix) aims to simplify the webpack configuration for code loading if you are using `.vue` files. This will automatically split up your html/css and javascript bvy using [vue-loader](https://github.com/vuejs/vue-loader) under the hood.

```
let mix = require('laravel-mix');

mix.js('resources/assets/js/main.js', 'public/js')
    .copy('node_modules/font-awesome/fonts', 'public/fonts')
    .sass('resources/assets/sass/app.scss', 'public/css')
    .version();
```


