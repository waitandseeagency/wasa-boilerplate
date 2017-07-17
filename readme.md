# WASA Boilerplate
A front-end boilerplate that's easy-to-use and ready-to-go.

<table>
  <tr>
    <td>
      <img width="77px" alt="Sass logo" src="http://www.johann-pinson.fr/img/data/wait-and-see-agency.png" />
    </td>
    <td valign="bottom" align="right">
      <a href="https://nodei.co/">
        NodeICO incoming
      </a>
    </td>
  </tr>
</table>

## Requirements
- node-js >= 6.4.0

## Installation
To automate the installation process, we recommend that you use the <a href="">wasa-cli</a>.

Otherwise, follow these instructions:
- `npm install` to install the dependencies.
- `npm install -g commitizen` to globally install Commitizen.

## Documentation

### NPM Scripts
The boilerplate is powered by npm scripts. No need of Gulp or anything else, as we are using the CLI services of Babel, Node-Sass, Pug (etc.). You can run each script individually. For each type of asset, there are two scripts. The first one builds them, and the second one build and watch for changes (e.g. `npm run babel` and `npm run babel:watch`). You can find every script in the section "scripts" of the file `./package.json`.

##### To start the server and watch the assets, use:
```
npm run
```

### Javascript
#### Configuration
We are not using nodejs requires as it is not compatible with modern browsers. As a result, import/requires/exports are not allowed. Every JS code must be written inside of a single file, located in `./app/scripts/index.js`

#### ES Linter
We are using the <a href="https://github.com/airbnb/javascript">Airbnb JavaScript Style Guide</a>. You can find the configuration file in `./.eslintrc`. The linter is not passing through our code. Instead, we recommend that you use a package within your text editor:
- Sublime Text: <a href="https://packagecontrol.io/packages/SublimeLinter">SublimeLinter</a>, <a href="https://packagecontrol.io/packages/SublimeLinter-contrib-eslint">SublimeLinter-contrib-eslint</a>, and <a href="https://www.npmjs.com/package/eslint">eslint<a/> (globally installed, `npm install -g eslint`).
- Atom: <a href="https://atom.io/packages/linter">linter</a> and <a href="https://atom.io/packages/linter-eslint">linter-eslint</a>. 

### CSS
#### Configuration
Every import is located in `./app/styles/index`. They are separated into five categories:
- abstracts: configuration and helpers.
- base: basic files (reboot, grid etc.).
- components: speaks for itself (e.g. Button).
- layout: layout-related sections (e.g. Header).
- pages: page-specific styles (e.g. homepage).

#### SCSS Linter
We are using the <a href="https://github.com/airbnb/css">Airbnb CSS / Sass Styleguide</a>. You can find the configuration file in `./.scss-lint.yml`. The linter is not passing through our code. Instead, we recommend that you use a package within your text editor:

- Sublime Text: <a href="https://packagecontrol.io/packages/SublimeLinter">SublimeLinter</a>, <a href="https://packagecontrol.io/packages/SublimeLinter-contrib-scss-lint">SublimeLinter-contrib-scss-lint</a>, <a href="https://www.ruby-lang.org/fr/">ruby<a/> and <a href="https://rubygems.org/gems/scss_lint">scss_lint</a>.
- Atom: <a href="https://atom.io/packages/linter">linter</a> and <a href="https://atom.io/packages/linter-scss-lint">linter-scss-lint</a>

### Git naming convention
We are using <a href="https://commitizen.github.io/cz-cli/">Commitizen</a> to automate our git messages. Simply add files to your commit and then run the command `git cz`. A prompt will appear and automate your process. By default, we are using the conventionnal-changelog convention (e.g. `'feat(boilerplate): init boilerplate'`).
