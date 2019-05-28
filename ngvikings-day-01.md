## Top things

- Angular Schematics

## John Papa

- Angular Launch Angular

- vikings2019-ext

## Kristiyan Kostado

- Angular CDK - building Angular Component library
  - Drag & drop

  - Virtual scroll

## Minko Gechev - https://github.com/mgechev

- Loadchildren -> dynamic import v8 👍

- "How we automated our Angular updates" -, medium.com

- https://update.angular.io

- How to contribute

  - Writing docs/posts

  - PR's

- Differential loading -> split build for older browsers

- Bazel  -> Alt for Webpack

  - WOn't build what hasn't changed

  - https://medium.com/lacolaco-blog/how-to-try-angular-cli-with-bazel-c133181d32da

## Shuela Jacobs `Chris Noring`

### NG-deploy

- Deployment made easy

- Build on top of Schematics

- https://github.com/Azure/ng-deploy-azure

========== TRACKS

## Sebawita - Nativescript

- NativeScript 

- Code sharing between Native and Web 

- Monorepo with all

- https://github.com/NativeScript/nativescript-schematics

  - Super easy migration from web-only project to web-and-native

- https://github.com/sebawita/angular-tour-of-heroes

## Alex Okrushko - NGRX

- Don't let users wait

## Aaron Frost - Lazy Loading Angular

- Presentation: https://docs.google.com/presentation/d/1p8Mzl2cNgCOIiDXk089QQcdLqNaGbiuGX-kUTaDsrhs/edit

- https://codeburst.io/how-to-implement-lazy-loading-in-angular-bb2a670b34d

- All re-used components are loaded in the common.js bundle, so not lazyloaded

- https://github.com/aaronfrost

### Lazyloading non-angular

- Add to tsconfig.json  inside compilerOptions:  "module": "esNext"

- Dynamic import 'library

- 'import('module').then(onfulfilled: module => console.log('loaded: ', module))

### Lazyloading angular

- angular.json "build.options" : "lazyModules": ['module1'

- https://www.npmjs.com/package/@herodevs/hero-loader

## Valentin Kononov - Bad practices in Angular

- https://slides.com/valentinkononov/angular-bad-practices

- @angular-devkit/build-optimizer pipable operator RxJsx

- TakeUnil is good to destroy the subscriptions

- Async pipe https://angular.io/api/common/AsyncPipe

- Use RxJs Tsling rules https://www.npmjs.com/package/rxjs-tslint-rules

- ngFor trackby  only updates the DOM not initials the whole component https://slides.com/valentinkononov/angular-bad-practices#/21

- Pipes will be cached https://blog.angularindepth.com/the-essential-difference-between-pure-and-impure-pipes-and-why-that-matters-999818aa068

- Pipe change detection https://excitoninteractive.com/articles/read/58/angular-user-interface-projects/pipes-and-angulars-change-detection
