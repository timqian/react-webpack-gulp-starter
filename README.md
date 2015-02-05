**react-webpack-gulp-starter**

One of the billion other custom starters out there.


*Note: Your desired **Flux** implementation can be easily mixed in (using [http://martyjs.org/](martyjs) as an example): `npm install --save marty`*

**Structure**
```
root
│   package.json - Contains the Jest configuration, dev and production dependencies
│   gulpfile.js - Loads tasks inside /tasks
└───src
    │   index.html
    │   index.js - Application main
    │   ...
    ├───assets
    tests
    │   preprocessor.js - JSX preprocessor for tests
    │   ...
    tasks
    │   ...
    ├───webpack
    │      webpack.config.js - Webpack configuration
    │      ...
```

**Setup**

1. Clone (or download)
2. Install Gulp globally `npm install -g gulp` (may require admin rights)
2. Under project root, run `npm install`
3. That's it!

**Tests**

The starter is set up for [https://facebook.github.io/jest/](Jest) (have a look at `package.json.jest`). Put your tests inside `/tests` and run `npm test`.

*Note: The test preprocessor `/tests/preprocessor.js` is set up to process the files with the .jsx extension as JSX and ignore .css files.*

**Development**

Run `npm run dev`. This command creates a `/dist` folder containing:

- `/src/index.html`
- All the assets under `/src/assets`

It also runs [http://webpack.github.io/docs/webpack-dev-server.html](webpack-dev-server) on `localhost:3000` with [https://github.com/gaearon/react-hot-loader](react-hot-loader)

*Note: The JSX loader for webpack `/tasks/webpack/webpack.config.js` is set up to process the files with the .jsx extension.*

**Release**

Run `npm run release`. This puts a `/dist` folder containing:

- `/src/index.html`
- All the assets under `/src/assets`
- Minified and bundled `bundle.js` and `bundle.css`

**License**

Licensed under WTFPL V2.