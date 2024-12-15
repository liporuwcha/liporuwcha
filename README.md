# liporuwcha

***Framework Stack Linux-Postgres-Rust-WASM-CSS3-HTML5-Axum***

 ![maintained](https://img.shields.io/badge/maintained-green)
 ![work-in-progress](https://img.shields.io/badge/work_in_progress-yellow)
 ![rustlang](https://img.shields.io/badge/rustlang-orange)
 ![postgres](https://img.shields.io/badge/postgres-orange)

 ![logo](https://github.com/liporuwcha/liporuwcha/blob/main/images/logo/logo_liporuwcha.png)  
 liporuwcha is a "GitHub organization" that groups [multiple repositories](https://github.com/orgs/liporuwcha/repositories?q=sort%3Aname-asc) together

 [![Lines in md](https://img.shields.io/badge/Lines_in_markdown-0-green.svg)](https://github.com/liporuwcha/liporuwcha/)
 ![liporuwcha](https://bestia.dev/webpage_hit_counter/get_svg_image/000.svg)

## Motivation

I would like to code some useful small programs. It is my hobby. These programs will live on the web. Why code anything else today?

Programming things from zero is not viable. Maybe for educational purposes, but it is not productive at all. I need a basic framework to build programs on top of it. Frameworks are both a blessing and a curse. They are productive for the use-case they are created for, but limit the freedom to code anything different.

This is not meant to be a commercial product or whatever. It is a reasonably usable and simple framework for hobby programs.

Without exceptions, sooner or later every program needs a database. I think Postgres is a great open source database. This is the main point of my programs: get some data from the user, transform it somehow and return it to the user in a different form. 90% of that is going to work inside the database. It is not great for scalability, but that is not a problem I will ever encounter.

The client cannot be connected directly to the database. That is a no-no. We need a web server with some middleware. I choose the Rust language and one of its library crates Axum for the web server.

The only client I need is a browser. All modern browsers work with HTML5, CSS3 and WebAssembly/WASM. There exists PWA/progressive web applications, electron or Tauri to make the web app feel like a native one. I think it is a good trick to make the client truly cross-platform.

This three-tier architecture has great potential. I don't see the point to make it any less flexible than that. There will be some complexity because of the three-tiers, but we will solve that somehow. The framework will have the tools to make our lives easier.

## Naming

Naming things is the major difficulty of programming. There is seldom a good name around. Usually when you choose one, you have to stick with it forever.

I choose the strange unique name **"liporuwcha"** for this project. It does not mean anything. It is barely pronounceable. It is an abbreviation of the Stack Linux-Postgres-Rust-WASM-CSS3-HTML5-Axum. This will be the name of my "framework". On top of this framework it will be relatively easy to add functionality or different apps.

The nature of three-tier architecture makes it difficult to use just one specialized tool. So tooling is limited and I want to use namespaces to make code searchable through every tier. Search-all-and-replace will be most of my "intelligent coding tool".

I hope that the character "_" underscore is available everywhere. The names will use the snake case style like `abc_what_a_nice_name`. I choose that to avoid problems with case sensitive and not case sensitive languages and technologies.

## Namespaces

This project is way too complex that I would like it to be. But I must bite this sour apple. I cannot work on anything simple until I have this moderately complex framework. Things will be getting easier after finishing the framework.

I will try to split the project into many modules. Ideally the modules are layered in levels. The higher level module can have dependency on lower modules, but it is forbidden to depend in the other direction. This rule will sometimes complicate things, but the resulting code will be reasonably maintainable.

I hope I will not mess this up, because later it will be impossible to change the names and namespaces.

I think a three latter namespace is good for my use-case.
The first letter defines a big project, that is not dependent of what comes after it.

- a - development tools, infrastructure
- b - common code for the framework
- c - configuration, migration, updates
- d - authentication and authorization

letters in between are for future use

- z - webpage hit counter
    the first project on top of the framework

## a - development tools, infrastructure

Namespaces with 2 and 3 letters. This list will grow eventually.

aa - operating systems

- aaa - Linux
- aab - Windows
- aac - WSL on Windows
- aad - android
- aae - MacOS and iOS

ab - networks

- aba - tcp/ip
- abb - web http request-response
- abc - websockets
- abd - http2
- abe - http3
- abf - server side events

ac - postgres database

- aca - database servers
- acb - database config
- acc - tables, fields, indexes
- acd - views, procedures, functions,...
- ace - administrative tools inside the database
- acj - database editor

ad - Rust language

- ada - Rust language
- adb - cargo crate dependencies
- adc - cross platform compiling
- add - development container crustde
- adj - VSCode as Rust editor

af - AXUM web server

ai - SSR server side rendering

aj - client side rendering

ak - WASM, javascript

## b - common code for the framework

With this namespace I will have a working framework that works with database, server and client.
But without any content. It is the basis for later content.

ba - database core (common code)

bj - server core (common code)

bs - client core (common code)

## c - configuration, migration, update

Every project evolves and the code and the database need to be updated. Sometimes it is called "migration". Living with a database is very dynamic. Much more than just living with a program.

The same database can contain more than one project coded by different teams. The order of changes must not be linear. It means, that the team must know what projects are exclusively theirs and what projects are common and must be coordinated with other teams.
When writing the code it must be always careful, that it does not break when a new field is added.

To achieve integrity of the database all the code is concentrated inside the database. So other parts of the project can use common code.

Here we need backup and restore and we need Development, Testing and Production environments.

ca - tables, fields, relations, views, procedures, configuration

cj - migration:  
how to migrate every table separately. Ideally without server downtime.

## d - authentication and authorization

Nothing serious cannot be done without authentication and authorization.

da - authentication

dj - authorization

## Open-source and free as a beer

My open-source projects are free as a beer (MIT license).  
I just love programming.  
But I need also to drink. If you find my projects and tutorials helpful, please buy me a beer by donating to my [PayPal](https://paypal.me/LucianoBestia).  
You know the price of a beer in your local bar ;-)  
So I can drink a free beer for your health :-)  
[Na zdravje!](https://translate.google.com/?hl=en&sl=sl&tl=en&text=Na%20zdravje&op=translate) [Alla salute!](https://dictionary.cambridge.org/dictionary/italian-english/alla-salute) [Prost!](https://dictionary.cambridge.org/dictionary/german-english/prost) [Nazdravlje!](https://matadornetwork.com/nights/how-to-say-cheers-in-50-languages/) 🍻

[//bestia.dev](https://bestia.dev)  
[//github.com/bestia-dev](https://github.com/bestia-dev)  
[//bestiadev.substack.com](https://bestiadev.substack.com)  
[//youtube.com/@bestia-dev-tutorials](https://youtube.com/@bestia-dev-tutorials)  
