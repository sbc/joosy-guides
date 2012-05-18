---
layout: index
title: "Getting started"
---

## Getting started

### The most important thing to know

Joosy is not an MVC framework. It addresses the same problems but it's not based clearly on a popular MVC paradigm. Nor it is an MVVM. Joosy is an active view for your server-side framework (mainly the Rails). It was created to complement and cooperate with backend. Not to be an abstraction. Therefore you'll probably like it if you are:

* Rails developer
* Use CoffeeScript heavily
* Like HAML (not really required)

The first point is required to fill Joosy the right way. It was greatly inspired by the approach Rails promotes. Unlike most of alternatives we don't stay away from a real-life troubles. Nor we expect the community to decide on it's own. We try to give some kind of convention for each of them. Just like in Rails you should concetrate on what you do. Not how you do it.

CoffeeScript is an alma-mater of Joosy. In theory you can use Joosy with a plain JS but you won't be happy. We use the Coffee meta posibilities heavily. Joosy is class-based and relays on CoffeeScript static methods prototype magic. Without having requirement to stay JS-compatible we created an interface that is as clear as possible.

We've added some spice to the Rails+Coffee combo. Applause, the Sugar.js. This incredible library extends the JS the way you are used to with an ActiveSupport. All the comfortable features are here: `[].first`, `'foo'.camelize`, `'fluffy'.pluralize` and many-many more. This sause really make the Coffee feel just like Ruby.

And last but no the least: viva la HAML! Joosy uses templaters abstraction so in theory you can use anything you are used to. But if you ever tried HAML and fell in love like we did, Joosy is shipped with amazing HAML-Coffee template engine.

### Not am MVC? But...

The idea is simple. REST in not an SQL. Application Server is not an RDBMS. You can't have real logic inside your models. Therefore you don't have models. Inside your browser you don't need to be linked to REST structure since your only goal is an interaction with user. That's why you don't need controller. Joosy operates with View terms. It has pages, layouts, widgets, forms. Everything you are used to but with a Rails flavor.

With Rails you pass your data to your templates through controller and then get it back from forms or AJAX-queries. That's exactly how Joosy works. It has a layer of slim `Resources` (just like `@foo` that was sent to your view). Yes, they are pulled from REST controllers and not otherwise but does it change anything? As soon as you got your data from your controller you operate with a `Layout` and `Pages`. Each of them is a entity that hold interaction with users. It's connected to a template, JS events and all that stuff you expect from your browser application. To avoid redundancy you can group typical code into something that is called `Widget`. Joosy controls your DOM so it only reloads layout when the new page requires another one.

To send data back Joosy has a `Form`. It wraps your basic HTML form and turns it into AJAXified thing. It works without page reload and interacts with your code using events. It even has an event for the "upload progress". `Forms` are magically linked to `Resources` so you don't write your code twice. Wait, even more! You have the `formFor` helper. Just like in Rails.

As mentioned before Joosy uses HAML-Coffee template engine. Joosy supports helpers we love so much. Again, just like Rails.

Offcourse we have other stuff like `Router` and `Preloader`. Everything out of box.

### Okay, it's Rails. Anything else?

Unlike Rails server application it has a state. For example if you use the only `Layout` for every page it will never get reloaded. Unlike the data it holds. To ease the DOM updates Joosy has `dynamic rendering` feature. It allows you to bind your resource to a template to automatically update DOM whenever resource changes. No manual events handling and rerendering. You just call `@renderDynamic` for a partial and it always stays actual.

Besides that Joosy offers built-in Identity Map implementation. You don't have to care about `Resources` instances. Even if you reload your `Resource` from a new Page your dynamic rendering will work from your Layout. Or any other place.

### Total highlights

Just to make sure you get it right here's the full list of functionality highlights we have to offer:

* Easy and familiar Application structure. You work with pages, layouts and forms.
* Built-in ActiveSupport analog
* Built-in HAML-Coffee templates
* Helpers
* Identity Map for your data
* Easy and straightforward dynamic binding of data to a DOM
* Built-in preloaders
* Automatic Resources generation based on Rails REST routes
* Out-of-box code generators
* ActiveResource-like REST interface

### So what is Joosy good for

Joosy is intended to ease building of modern medium and large-sized browser-based applications using Rails as a backend. To minimize code base while providing more features and what's most important, giving you ready conventions for typical tasks.

Compare Joosy to Backbone like Rails to Sinatra. While Rails engine is much more powerful, Sinatra still has a lot of cases to be used at. If all you need is to enable some RICHness on one of your pages, Joosy can handle that. But Backbone will do the trick with lesser dependencies. If you need to move complete web-resource to browser Joosy will do the task at its Best.

So what are you waiting for? [Go look for some guides!](/)