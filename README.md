# Micro-frontends with SvelteKit

Sample POC application to develop Micro-frontends using SvelteKit.

## Application Shell

This repository contains the code for the application shell. Sub-modules can be added to the modules folder inside the routes folder. The modules folder is added to the .gitignore so that any changes to the modules will be ignored in the application shell repository.

## Creating a module/working with module

Clone a repository associated with any sub module into the modules folder as in the following.

```bash
mkdir module-first
cd module-first
git clone https://github.com/gvkumarreddy/svelte-micro-frontends-module-first.git .

```

> Note: the `module-first` is a module name

The above sample module uses a common component by name `Draggable` from the `app-shell` repository (The current repository).

There is a navigation link added to the above module in the file `src/lib/Header/index.svelte`

With the simple approach as above, we can create as many modules as required and the individual teams can work in their respective sub-modules.


## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

Before creating a production version of your app, install an [adapter](https://kit.svelte.dev/docs#adapters) for your target environment. Then:

```bash
npm run build
```

> You can preview the built app with `npm run preview`, regardless of whether you installed an adapter. This should _not_ be used to serve your app in production.

## Feedback

Any suggestions or feedback? Email me at `gvkumar.reddy@gmail.com`