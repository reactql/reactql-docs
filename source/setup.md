---
title: Setup & Installation
sidebar_title: Installation
description: How to deploy ReactQL for your next project
---

<h2 id="what">System requirements</h2>

This starter kit is built primarily for OS X, but should work with most flavours of \*nix and Windows (hopefully.)

You'll need [Node.js](https://nodejs.org) installed.

<h2 id="new_project">Starting a new project</h2>

---
Simply clone the starter kit:

```bash
git clone --depth 1 https://github.com/leebenson/reactql <project_folder>
```

... then install the required packages:

```bash
cd <project_folder>
npm i
```

... and start writing over it.

In future, you'll be able to install globally via NPM and generate projects with a few other goodies such as code generation, deletion of the `.git` folder, etc.

<h2 id="development">Running in development</h2>

---
In development, ReactQL will:

- Run a development server at [http://localhost:8080](http://localhost:8080)
- Build a browser-side bundle only
- Enable sourcemaps for your CSS and Javascript code
- Activate hot code reloading; any changes to your code will update automatically in the browser

To activate development mode, run:

```bash
npm start
```

Changes to your React components/styles will update in the browser in real-time, with no refreshes. Changes to other code may require a refresh.

<h2 id="production">Bundling for production</h2>

---
In production, ReactQL will:

- Build a server bundle, which includes a built-in Koa web server
- Activate server-side rendering (SSR) for your React components / GraphQL data fetching
- Create a minified browser bundle
- Crunch your CSS, images and other web assets

To run it, you first need to build the server and client bundles with:

```bash
npm run build
```

Then, simply run:

```bash
npm run server
```

... which (by default) spawns a server at [http://localhost:4000](http://localhost:4000)

Or, you can run the short-cut: `npm run build-run`, which has the same effect as running the above two commands separately.