# Material Check

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

## FAQs

### How do I add angular material style?

Installing with `ng add @angular/material` (a new feature of angular 6) did not work. So, angular material has to be added the old way (together with `@angular/cdk` and `@angular/animations`):

```
npm install @angular/material @angular/cdk @angular/animations
```

Add material core theme to `styles.css`:

```
@import "~@angular/material/prebuilt-themes/deeppurple-amber.css";
```

Alternativelly, you may customize the material style. Rename `styles.css` to `styles.scss` (and adjust name in `angular.json`) and add your style.

Add `BrowserAnimationsModule` to app.module.ts

```
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
...
imports: [
    BrowserAnimationsModule,
    ...
]
```

Finally, add a link to the icons in `index.html` as they are not delivered in the librariesx§x:

```
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
```

Now, you are ready to add material starter components.

Add navigation starter component with `ng generate @angular/material:material-nav --name=my-nav`

However, `ng serve` will fail. Fix my-nav.components, see https://github.com/angular/material2/pull/11448/commits/20306dbeed3fe7232ffb85ba1d9fd406f6885db2

Add dashboard starter component with `ng generate @angular/material:material-dashboard --name=my-dashboard`

Add table starter component with `ng generate @angular/material:material-table --name=my-table`

