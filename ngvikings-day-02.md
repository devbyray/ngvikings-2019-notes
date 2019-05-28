

# Day 2 - Keynotes



## Matt Podwysocki - Wahlin - An async journey

- https://twitter.com/mattpodwysocki
- Design Patters - Elements of reusable OO software - 1994 book (Observer - Event)
- Functional Reactive Programming - Behaviour & Event - 1997 
- Monads??
- ReactiveX - API for async programming with observable streams - JavaScript, Java, C#, Go, C++ etc. http://reactivex.io/
  - Iterable
  - Observable
  - Object
  - Promise
- Steap learning curve
- You can cancle a Observable  -> A promise not
- You stay subscribed to a Observable untile you unsubribe
- IXJS - https://github.com/ReactiveX/IxJS



## Dan Wahlin - Angular Architecture Concepts

- https://twitter.com/DanWahlin

- Presentation: https://docs.google.com/presentation/d/1zayHhGRCe3bdPu9ZRxc54TXFxvZYyvoMmqIoR6c8Z60/edit

- Architecture planning

  - Overview of your app you planning to build

  - Features of the app

    - important for your modulel design

  - Domain security

    - Think about what backend is gonna secure the application

  - Domain rules

    - What is gonna happen serverside or clientside

  - Logging

    - Serverside logging

    - To see what is happening

  - Services/communication

    - What kind of services

    - Is there any realtime communication

  - Component organisation

  - Shared functionality

    - Libraries

- Module organisation

  - Just like organising Lego

  - Component communication

- Features Modules https://angular.io/guide/feature-modules

- Container and Presentation component

  - Container component gets the data via a service

  - Container component with stupid component that don't know where the data is comming from

  - Set change detection to **OnPush** in presentation components. This is to prevent to renew the whole DOM

  - Presentation components won't chang and ngOnChanges won't fire

- Component communication

  - Don't do input to input to input (or output)

  - Create a service *EventBusService* to send data to great parents components (mediator pattern)

  - Observable service to send data to great parents components. Share data between components via a BehaviorSubject asObservable

- Do you need a state-management library?

  - A lot of times you don't need a state-managment lib

  - Sharing date between component via a service

  - Observable Service (not in to much complex)

  - NGRX

  - NGRX-data (*new*) much simpler

  - Observable Store (recommended) based on RxJS

  - MobX

  - Akita

  - NGxs

- Tips

  - Spend time planning your architecture

  - Take a feature based approach to module org

  - Leverage observables for communication

  - Question if you need a state managment solution



## Kenneth Rohde Christiansen - PWA, Web Platform, Chrome

- Web Share

- Recieve shares

  - Web share target

- Media session AP for media playing

- Shape detection api for QR codes, faces, payments

- Badging for badges in the icons on desktop

- Wake lock, prevent from display of or prevent system go of (WIP) https://developers.google.com/web/updates/2018/12/wakelock

- File system

  - Handy for video or image editors

  - Or do VSCode on the web and save to your file system from the browser

- Serial API 

- WebHID (game controllers via Bluetooth)

- Contacts picker, sharing contacts with a website

- Font Access API simplify us of locally installed fonts

- Sources: https://codelabs.developers.google.com/codelabs/web-capabilities/index.html



# Day 2 - Tracks



## Filip Bech-Larsen  - Frameworks and webcomponents

- https://github.com/filipbech/framework-webcomponents

- Webcomponents

  - Portability

  - Native components brings native performance

  - Framework === implementation detail

  - Great browser support, soon without polyfill

- Specs

  - Custom elements

    - Define your own elements

  - Shadow DOM

    - Get default styling 

  - Template element

  - ES-Modules

    - Import and export JavaScript modules

- Create super simple custom elements, it's a class that extends HTMLElement that's defined in JavaScript

- Properties vs attributes

  - You can pass anything to properties

- Styling

  - With scoped to shadowRoot

  - custom-properties

  - sepecial selectors - :host, :slotted

  - ::parts on the horizon

- With frameworks

  - How to use web components in Angular, Vue, React (preact)

  - https://custom-elements-everywhere.com/

  - Angular and Vue are scoring 100% with Webcomponents support

  - React score is 71% with Webcomponents support

  - Preact score is 91% with Webcomponents support



- Write your custom element in a framework of choice and get used by other frameworks

  - With Native Webcomponent framework

  - Wrap in custom-element

- Wrapping

  - Elements-props for data

  - Dom-events for events

  - slots

  - Shadow dom 

- Export to webcomponents

  - Angular: https://github.com/chriskitson/custom-element https://alligator.io/angular/using-custom-elements/

  - Vue: https://github.com/vuejs/vue-web-component-wrapper https://alligator.io/vuejs/vue-integrate-web-components/

  - React: https://github.com/bspaulding/react-custom-element

- Example

  - Angular: https://github.com/jeroenouw/AngularElements



## Mike Hartington - Ionic

- https://capacitor.ionicframework.com/docs/

- https://twitter.com/mhartington

## Kwinten Pisman - Angular in a Microservices

- https://twitter.com/KwintentP

- Angular Checklist https://angular-checklist.io/projects

- StrongBrew https://blog.strongbrew.io/

- Microservices - Independent deployable

  - Lack of communication between teams/applications

  - It's better to think about teams develop features, so things will be more shared accross teams and applications

  - Sharing code between applications by using NPM

  - Monorepo will make sharing code a lot easier.

    - Upgrading dependencies

    - 1 linter and config file for the repo

    - Monorepo !== Monolith

  - https://nx.dev/

    - NX will help building a Angular Monorepo

    - Create workspaces

      - Apps folder

        - Webshop app

        - Stock management app

        - etc...

      - Lib folder

      - Generate app for every application

      - Link libraries in the tsconfig.json

    - NX can generate a demo-graph of all the modules with dependencies

      - This gives insights over what to test when a feature is changed, to you know what modules are depending on it.

      - yarn affected. This will show what is impacted by our changes https://blog.nrwl.io/nrwl-nx-6-1-better-dev-ergonomics-faster-builds-3198bb310e39

      - If you don't have a monorepo, you're not really doing CI, you're doing frequent intergration at best. ***Alex Eagle***

  - Summary

    - Let applications be build based on a range of features so code sharing is easier.

    - Building a lib inside a monorepo is easier to update, because all the dependencies are equal in every application






