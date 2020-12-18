# svelte app

This is a project that demonstrate an issue with dynamic imports with Svelte custom elements. Lazily loaded Svelte custom elements stop reacting to any properties changes that were assigned to the component before hydration.


## Get started

Install the dependencies...

```bash
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see the app running.

## Issue Details

A custom element is stamped in the dom as a simple HTML element until the component is imported. Binding props to this simple element creates a variable in the component, e.g. component.someProp which overrides the default setters and getters of Svelte of the same name (get someProp, set someProp) after the custom element is loaded.