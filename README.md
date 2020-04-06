# Blank React App on Parcel

## Frontend

### Setup

1. Install Nodejs

2. Package manager

```bash

mkdir reactapp
cd reactapp
npm init

```

3. Bundler

```bash
mkdir src
npm install --save-dev parcel-bundler

```

Open your package.json file, and add this field:

```js
{
  ...
  "scripts": {
    "dev": "parcel src/index.html",
    "build": "parcel build src/index.html"
  }
}
```

4. Compiler

That means Babel

Parcel comes built-in with a default Babel configuration that uses the babel-env and browserslist.
The browserlist target defaults to: > 0.25% (Meaning, support every browser that has 0.25% or more of the total amount of active web users).

The only thing missing is the configuration for compiling React-specific stuff like JSX. For that, we just need to install two packages:

```bash

npm install --save-dev @babel/core @babel/preset-react

```

And add a .babelrc.json file:

```js
{
  "presets": ["@babel/preset-react"]
}
```

5. Workflow

Your typical edit-save-refresh workflow would look something like this:

  1. In a Bash terminal run the command `npm run dev`. This starts Parcel’s development server and hot module replacement.
  2. Open your local site (defaults to http://localhost:1234) in your browser.
  3. Add, edit source files in the src folder using your editor/IDE.
  4. As you change and save files, Parcel will automatically refresh the browser.
