<p align="center">
<a href="https://vtec.okami101.io" target="_blank" rel="noopener"><img src="https://vtec.okami101.io/logo.png" width="300"></a>
</p>

<p align="center">
<a href="https://npm.okami101.io/-/web/detail/vtec-admin"><img src="https://img.shields.io/npm/v/vtec-admin.svg?style=flat-square" alt="Latest Version on NPM"></a>
<a href="https://npm.okami101.io/-/web/detail/vtec-admin"><img src="https://img.shields.io/npm/l/vtec-admin.svg?style=flat-square" alt="License"></a>
</p>

# Vtec Admin

SPA admin library for Vue.js running on top of REST APIs, built on Vuetify and comes with dedicated [Vue CLI plugin](https://npm.okami101.io/-/web/detail/vue-cli-plugin-vtec-admin) for 🚀. Ready to use on Laravel API backend by using official [Vtec Laravel Crud](https://github.com/okami101/vtec-laravel-crud) composer package, but can be used on every backend of your choice with your own data and authentication providers.

> See [full documentation](https://vtec.okami101.io)  
> Check [online demo](https://vtec-bookstore-demo.okami101.io) -> go to admin and use prefilled login (read only)  
> Note : this project is heavily inspired by [React Admin](https://github.com/marmelab/react-admin/) made by awesome [Marmelab Team](https://marmelab.com/)

[![demo](https://vtec.okami101.io/assets/screenshot.png)](https://vtec-bookstore-demo.okami101.io)

## Disclaimer

As this project was entirely made on my personal free time while I'm employed, and is totally free of charge, don't expect any support of anything. This project was just mainly a personal challenge and only aims to satisfy my own needs on personal projects. If you want to stay on full admin SPA land and for critical production usage or professional B2B sites I strongly advise you to go with [React Admin](https://github.com/marmelab/react-admin/) which is far more mature with high community or use [Nova](https://nova.laravel.com/) for Laravel for highest productivity with nice UI.

## Features

* Powered by Vuetify.
* Full standalone UI SPA admin that can be adapted to any backend (REST, GraphQL, SOAP, etc.) by writing your own data and auth providers by following specific contracts which ensure compatibility.
* Bare minimal Vue.js code needed to get your CRUD pages working via [DSL](https://en.wikipedia.org/wiki/Domain-specific_language) approach.
* [Vue CLI plugin](packages/cli) provided for immediate quick start while including nice [material theme by Creative Tim](https://github.com/creativetimofficial/vuetify-material-dashboard). Can be used on any Vue.js based application as well.
* 100% Vue CLI friendly. The Vtec Admin library is simply a plugin which integrates within all of your existing plugins, notably Vue Router, Vuex and Vuetify. Keep total control of your Vue app by adding your own routes with custom pages, custom store modules, and full Vuetify theming as you are used to on Vue CLI base project.
* Ready to use data provider for Laravel within [Spatie Laravel query builder](https://github.com/spatie/laravel-query-builder) .
* 3 auth providers included : the recommended cookie based authentication  for [Laravel Sanctum](https://github.com/laravel/sanctum), stateless authentication by JWT (tested with [Laravel JWT](https://github.com/tymondesigns/jwt-auth)), and simple basic HTTP auth for lazy guys...
* Simple guest authentication support if no auth provider transmitted.
* Advanced user permissions helpers for hide/show some UI components or menu links 🔒.
* Official separate [Vtec Laravel Crud](https://github.com/okami101/vtec-laravel-crud) package provided for insane quick start from top to bottom. Provides many backend features as spa authentication, profile editing, users management, impersonation, [translatable fields](https://github.com/spatie/laravel-translatable), [media support](https://github.com/spatie/laravel-medialibrary), [file manager](https://github.com/Studio-42/elFinder) with Wysiwyg bridges, etc.
Allow immediate start developement from backend to UI with already basic functional admin 🚀.
* Stay as little magic as possible by fully respecting each backend and frontend development environnement. If you know well Laravel and Vue CLI basics, so you're ready to go !
* Automatic guesser CRUD pages by default which take the best suited typed field or input from given value of each resource object property. As this pages are not really suited for production, they show full Vue.js template generated code as starter kit for your own templates !
* CRUD code generator commands on both Laravel and Vue CLI for even quicker ready-to-go API and UI base code.
* With usage of Vtec Admin, code generators as well as Vue.js power, feel the better mix between productivity, nice development experience and limitless customization ⚡.
* Full featured bookstore demo application, with [Laravel backend](examples/laravel) running on Docker and his associated [Vue CLI admin project](examples/demo) using [Vtec Admin](packages/admin).
* [Complete documentation](https://vtec.okami101.io) 🗄.
* Full intellisense support for all Va Components on Vetur and Jetbrains products 📃 !
* Internationalization support via Vue I18n, include english and french translations. Can be easily configured by taking user browser language 🌍.
* Translatable resource fields by contextual language selection on each crud page.
* Unique v-model context by form for minimal boilerplate code.
* Server-side form validation support.
* Many fields and inputs components for various data types: select, boolean, number, rich text, etc.
* Autocomplete input with entity reference support.
* TinyMCE 5 as default Wysiwyg with elFinder bridge, can be replaced by your own.
* Create your own fields and inputs simply by extending mixins.
* Full-featured DataTable, including multi-sort, pagination, global search, advanced filters, basic CSV export, live query string context. And of course with possibility of cell templating.
* Data iterator decoupled from datatable which allows you total customization of list layout.
* Advanced as-you-type filters with many supported inputs: select, boolean, autocomplete for search by relations, with multiple, etc 🔍.
* Customizable by-row, bulk and global actions.
* Direct aside create/edit from list instead of separate crud page.
* Support of resources association and dissociation for relationships 🍻.
* To finish, for what it's worth, it's completely free of charge 🤑.

## Why ⏩Vtec⏪

`vue-admin` was obviously already taken on NPM registry and `vuetify-admin` seemed to me to much UI related. I wanted to keep VA acronym. I'm a big fan of 90' Japanese cars and I remembered VTEC acronym from Honda, a system designed for power optimization at low and high speed. So I found it very suited for this project, which tries to deliver high efficency from top to bottom.

## Installation

Select your most suitable guide :

* If you choose Laravel as backend, follow [this optimized guide](https://vtec.okami101.io/guide/laravel.html).
* For all other cases, follow [the standard Vue CLI path](https://vtec.okami101.io/guide/getting-started.html).

## At a glance

See [this documentation section](https://vtec.okami101.io/guide/getting-started.html#at-a-glance) for quick code samples of admin initiatization and each CRUD page.

### Architecture

![Architecture](https://vtec.okami101.io/diagrams/architecture.svg)

> See how it works [here](https://vtec.okami101.io/guide/#how-it-works).

## Note on this main repo

It's contains all necessary projects to develop Vtec Admin and run demo and tutorial :

* [Vtec Admin Library](packages/admin), the main admin library.
* [Vtec Admin Vue CLI Plugin](packages/cli), the associated Vue CLI plugin which contains all base code boilerplate for quick install and UI commands code generator.
* [Vtec Laravel Crud](vtec-laravel-crud), git submodule of composer package to use on fresh Laravel project which facilitates Vtec Admin integration and includes server-side API commands generator.
* [Bookstore Admin Demo](examples/demo), full-featured admin sample build on top of main Vtec Admin Library.
* [Bookstore Laravel Demo](examples/laravel), suitable API backend for bookstore admin demo based on Laravel.
* [Admin Tutorial](examples/tutorial), finished tutorial after following [dedicated docs](https://vtec.okami101.io/guide/tutorial.html) which aims to made a good showcase of YAML code generation power.
* [Vtec Docs](packages/docs), vuepress docs.

> All of this projects are automatically linked together by symlinks thanks to yarn workspaces and composer for best library development experience. HMR from demo to admin library side-by-side is fully supported !

## Usage

### How to run demo locally

Be sure to have cloned this repo with git submodules. If not the case use `git submodule init && git submodule update`. [Vtec Laravel Crud](vtec-laravel-crud) should be cloned.

Requirements :

* `Yarn`.
* `Docker` with compose, required for quick-start run backend API. If you don't want it, follow [dedicated instructions](examples/laravel#classic).
* `Make` for easy starting all necessery tools. For Windows users install it via [scoop](https://scoop.sh/) with `scoop install make`. Use `make help` for all detail commands.

In order to run demo :

```bash
yarn # intall all yarn dependencies
make run-laravel-demo # run server api through docker (take a coffee if 1st time...)
make prepare-laravel-demo # initialize laravel app and inject dummy data (use it only at 1st launch)
make run-demo # compile all bookstore demo admin with HMR dev mode enabled
```

Admin panel should be autostart to [http://localhost:8080](http://localhost:8080).

### Run and build docs

Docs are hosted by VuePress. Use `make run-docs` to launch it on [http://localhost:9000](http://localhost:9000). `make build-docs` will generate static files inside `docs` root folder.

> API documentation for all VA components are autogenerated from source code thanks to [Vue Docgen API](https://vue-styleguidist.github.io/docs/Docgen.html).

## But why another admin panel again

See [guide intruduction](https://vtec.okami101.io/guide/#purpose) for real purpose of this project.

### Place of this project within other admin frameworks

So many admin panel are generaly tightly coulpled with backend framework and prevent us to switch easily. Besides most of the time it stays classic server-side templating engine oriented associated to good old jQuery plugins, with no usage of a powerfull UI framework as Vue.js. I think notably on [Backpack](https://backpackforlaravel.com/) for Laravel and [EasyAdmin](https://github.com/EasyCorp/EasyAdminBundle) for symfony world. The main advantage of this admin panels is to be highest productive as possible (and plently featured in case of Backpack) but tends to come with their own logic and stay first of all very configuration oriented.

On the other side, the official [Laravel Nova](https://nova.laravel.com/), although it is a very productive Vue SPA admin, with high community, isn't free, "closed" source, still Laravel-coupled and come with his own caveats. You tend to follow the "Nova" way with unnatural mix of coupled PHP and Vue development.

[React Admin](https://github.com/marmelab/react-admin/) (RA) is by far the coolest and most customizable admin panel on the market. Besides it's totally free and totally independent of any backend. Althought it isn't probably the more productive way to build basic admin app from top to bottom with backend included, this is in my opinion the funniest way to build admin apps, just as LEGO&copy; !

But I'm a Vue.js fan and I didn't find a close equivalent based on it. So why not to try a make one, mainly for "fun" and hard training ? I decided to take Vuetify as main UI library. The default layout is well suited for admin app, full of input components, and comes with data iterator which allows full list customization.

> Maybe you can check [`Vue Admin`](https://github.com/Cambalab/vue-admin)

### But I prefer Bootstrap

So this project isn't for you. All VA UI components are tightly coupled with Vuetify, and I have really no intention to decoupled them as React Admin does with separated controllers, it seems simply to much work for me.

Check [CoreUI](https://coreui.io/) project or try this [bootstrap UI layer](https://bootstrap-styled.github.io/react-admin/) for React Admin.

### Case of API backend

By its nature, RA doesn't propose any helpers for backend framework. [Api Platform Demo](https://github.com/api-platform/demo) does awesome work for Symfony area with full Swagger autogeneration, although it's can be the PHP annotation hell.

So I choose to make a [complete helper package](https://github.com/okami101/vtec-laravel-crud) for Laravel in order to have the best quick start experience possible, combined to generators for high productivity, while highly respecting the pure traditional Laravel way to make CRUD resources. I included YAML based code generators, similar as [Blueprint](https://github.com/laravel-shift/blueprint), with far less features to confess.

## State of this project

> This is a really alpha state package, without any unit tests or CI, so plenty of bugs and BC possible on every releases. Don't waste your time of using it for real projects, only for adventurers !

Many of React Admin existing features has been transposed in this project, but without client-side data cache and optimistic UI which necessit many work for something I don't really need. Besides this feature undercut server-side validation.  
Client-side lazy and eager relationships fetching is not included as well, because I prefer it on server-side. It's ok if you have full control of backend.

This app is of course far to be as sharp as RA which is the admin panel I highly recommended you to use for business apps. Moreover RA has really fast growing contributions and tends to be the "de facto" standelone SPA admin.

More backend showcase examples as Symfony / NestJS / Spring Boot / ASP.NET Core in addition to existing Laravel would be nice but it asks really too much work for now, especially if I should develop a dedicated API Crud composer / npm / maven / NuGet packages for each...

## Inspiring projects

### Standelone SPA admin panel builder

* [React Admin](https://github.com/marmelab/react-admin/), totally free and independent of any backend. Just build admin panel as LEGO&copy; ! Not the most productive as is (no backend helpers if we exclude [Api Platform](https://github.com/api-platform/api-platform)), and highest learning curve compared to the others.

### Free Symfony classic admin panel

* [EasyAdmin](https://github.com/EasyCorp/EasyAdminBundle), standard admin builder, not many widgets by default but very efficient and heavily configurable by YML config files and extendable with twig templates.
* [Sonata Admin](https://github.com/sonata-project/SonataAdminBundle), super massive admin builder, maybe one of the most powerful and full featured free admin panel on the market, but not really the most seamless development experience (personal opinion).

### Some Laravel admin panels

* [Backpack](https://backpackforlaravel.com/), not free for commercial projects, with the good old school HTML jQuery. Can have quickly bloated code in case of specific custom development needs, but still stay one of the most productive admin panel on the market with a tons of widgets.
* [Official Laravel Nova](https://nova.laravel.com/), not free and the most expensive, but full featured and very efficient SPA admin builder for Laravel with Vue.js. Code as fast as Backpack but with modern UI Framework and nice Laravel-ish development experience.
* [Voyager](https://voyager.devdojo.com/), free admin panel for Laravel.

## Full documentation

Full documentation can be found on the [Vtec docs website](https://vtec.okami101.io).

## License

This project is open-sourced software licensed under the [MIT license](https://adr1enbe4udou1n.mit-license.org).
