---
title: Vite

byline: |
   Next generation frontend tooling. It's fast!
key_links:
  homepage: https://vitejs.dev/
  repo_nwo: vitejs/vite

link_sections:
  - title: Templates
    links:
      - title: Vite Quickstart
        url: https://github.com/MichaelCurrin/vite-quickstart
      - title: React Vite Quickstart
        url: https://github.com/MichaelCurrin/react-vite-quickstart
      - title: Vue Vite Quickstart
        url: https://github.com/MichaelCurrin/vue-vite-quickstart
      - title: Community templates
        url: https://github.com/vitejs/awesome-vite#templates
tutorials:
  - title: Learn Vite with Evan You
    url: https://www.youtube.com/watch?v=DkGV5F4XnfQ
    description: A short video on YouTube that got me into Vite
  - title: 'A Vite demo | Evan You'
    url: https://www.youtube.com/watch?v=Pgsges6rw0o

  - title: 'How You Can Speed Up Your Development With Vite 2.0 | Create Fast Vue 3 apps with Vite 2.0 Tutorial'
    url: https://www.youtube.com/watch?v=SGIAwj3wp-o
  - title: Vite 2.0 Crash Course | Super Fast Build Tool for JavaScript, React, Vue, Svelte, & Lit (2021)
    url: https://www.youtube.com/watch?v=LQQ3CR2JTX8
---

## What is Vite?

Vite, pronouned "veet", is the French for "quick".

It's modern JS web development tool that works with plain JS and frameworks like Vue and React.

## Features

- Uses ESBuild internally for speed, which is built in Go and handles bundling about 30 times faster than using Node.
- It handles TypeScript code by converting it to plain JS without you having to do an in between step. You still need to do you typechecks separately though.
- Bundles your installed NPM packages.
- Bundles your CSS from imports - these get added to your `index.html` at build time. No need for installing and using style loader plugins like in Webpack, which would add CSS to your JS and then add them to the page once JS is loaded.

## Comparison with Webpack

From [article](https://harlanzw.com/blog/how-the-heck-does-vite-work/)

Vite's core functionality is similar to using these together:

- [Webpack][] - which does bundling
- Webpack Dev Server - for hot-reloading dev server

But, Vite has some core improvements on developer experience:

- Faster app start time, regardless of app size
- Hot module reloading that is almost instant, regardless of app size
- Compile on-demand
- Zero configuration out of the box for many pre-processors
- Handles Typescript and JSX using ESBuild, for speed

Vite also works as a faster alternative to Vue CLI.

[Webpack]: {% link resources/javascript/packages/webpack/index.md %}

### Scaffold new project

See [Getting Started](https://vitejs.dev/guide/#scaffolding-your-first-vite-project) in the docs.

These commands do not require `vite` to be installed.

### Run and then choose

- NPM
    ```sh
    $ npx vite@latest
    ```
- Yarn
    ```sh
    $ yarn create vite
    ```

You'll get prompts to name your project, pick a framework, and then pick a a variant like TypeScript.

```
❯   vanilla
    vue
    react
    preact
    lit
    svelte
```

#### Create by name and template

Or pass your choices in one command.

- NPM
    ```sh
    $ # V7+
    $ npx vite@latest my-vue-app -- --template vue
    $ # V6
    $ npx vite@latest my-vue-app --template vue
    ```
- Yarn
    ```sh
    $ yarn create vite my-vue-app --template vue
    ```

Here using Vue template for Vite, as per Vite docs and [Vue docs](https://v3.vuejs.org/guide/installation.html#vite).

See [MichaelCurrin/vue-vite-quickstart](https://github.com/MichaelCurrin/vue-vite-quickstart) for the result.
