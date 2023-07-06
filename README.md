The app is built in svelte. In order to use svelte you must have node.js/npm (node packagae manager) installed. 

## Svelte Instructions

### Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

### Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
## Breakdown of Files
### src/components 
src/components contains the components that make up the app. The global component is App.svelte, which creates the visible application. The components are named according to their actions (i.e. leaflet map is the component for the map, tooltip is the component for the tooltip). These behave intuitively with one tricky exception: the chart container is inside the leaflet map (rather than in App.svelte) in order to allow for it to change dynamically according to the selected cities using svelte's built in dynamic updating.

### src/data
src/data contains the data that is behind the visualizations. Currently the data is just dummy data for a few cities but following the json format as seen (or updating it according to the desired categorical variables for the visualization) for other cities can follow a similar format for east use in the visualizations.

### src/routes
Currently, src/routes is not used, but if the web app were to have multiple pages, then this is the place you should add the multiple pages following to the format used so farr.
