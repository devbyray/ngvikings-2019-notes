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

  - If 
