# Angular-8 Interview Questions & Answers

> Click :star:if you like the project. Pull Request are highly appreciated.

### Table of Contents

| No. | Questions |
|---- | ---------
| <span id="Q1">1</span> | [What is Angular 8?](#what-is-angular-8)|
| <span id="Q2">2</span> | [What is new in Angular 8?](#what-is-new-in-angular-8)|
| <span id="Q3">3</span> | [What are the building blocks of Angular?](#what-are-the-building-blocks-of-angular)|
| <span id="Q4">4</span> | [Which command is used to create service?](#Which-command-is-used-to-create-service)|
| <span id="Q5">5</span> | [What is use of `ngIf` directive?](#What-is-use-of-`ngIf`-directive)|

----
  _Questions_ <a href="#Q1">**1**</a> | <a href="#Q2">**2**</a> | <a href="#Q3">**3**</a> | <a href="#Q4">**4**</a> | <a href="#Q5">**5**</a> | <a href="#Q6">**6**</a> | <a href="#Q7">**7**</a> | <a href="#Q8">**8**</a> | <a href="#Q9">**9**</a> | <a href="#Q10">**10**</a>
  ----

1. ### What is Angular 8?

    Angular is one of the **most popular** and **open source Front-end or Client-side scripting framework** for building Mobile and Desktop Apps. Angular is written in TypeScript language and It is compiled into JavaScript. Angular community has released the latest version Angular 8 on **28 May 2019**. This version contains some of new features, lot of performance and Workflow Improvements.

  **[⬆ Back to Top](#table-of-contents)**   |   <a href="#Q1">**⬆ Back to Question 1**</a>

----
  _Questions_ <a href="#Q1">**1**</a> | <a href="#Q2">**2**</a> | <a href="#Q3">**3**</a> | <a href="#Q4">**4**</a> | <a href="#Q5">**5**</a> | <a href="#Q6">**6**</a> | <a href="#Q7">**7**</a> | <a href="#Q8">**8**</a> | <a href="#Q9">**9**</a> | <a href="#Q10">**10**</a>
  ----

2. ### What is new in Angular 8?

    *  Angular Ivy :
        
        *  Ivy is the new compiler/runtime of Angluar.
        *  It is the latest rendering engine but not defualt engine for Angular 8.
        *  It generates smaller bundles; faster compilation.
        *  It translates the templates and components in HTML and JavaScript.

    *  Support for TypeScript (Higher Version) : 

        * It supports TypeScript 3.4; no version below 3.4.
        * It is superset of javascript.
            <img src="images/typescript-javascript.png" width="200px" height="200px" float="right">
        * Points out compilation errors at development time only.
        * Object oriented programming language.
        * Introduces strong typing.
        * Portable across browsers, devices and OS.
        * At the end, In Angular; Typescript is converted into Javascript.

    *  Support for Bazel :

        *  Bazel is build tool developed and used by Google.
        *  The angluar community is working to integrate Bazel tool in to the standard angular toolset to enable developers to perform faster builds on large projects.
        *  It allows to deploy only what has been changed.
        *  Opt-in Option with Angular 8.

    *  Support for Web Worker Bundling :

        * Web workers allow you to run CPU-intensive computations in a background thread, freeing the main thread to update the user interface. 
        * If you find your application performs a lot of computations, such as generating CAD drawings or doing heavy geometrical calculations, using web workers can help increase your application's performance.

    *  New changes in ViewChild and ContentChild
    *  Builder API and Workspace APIs in the CLI
    *  Differential Loading by Default : 
        
        *  Creates two bundles which will be loaded according to the browser version and support : 
            1. ES6+ Bundle - For New browsers support; So that new browser loads less code to run the app in the browser.
            2. ES5 Bundle - For Old browsers support; So that old browser loads more code to run the app in the browser.

    *  Improvements in AngularJS Migration
    *  Lazy Loading with Dynamics Imports :

        *  Delay the loading of an object until it is required.
        *  Features loaded only when user the user navigates to their routes for the first time.
        *  Keeps the initial bundle size smaller; decreases load time. 
        *  Standard dynamic import syntax is  used.

        *   ```typescript
            const routes: Routes = [
            {
            path: 'items',
            loadChildren: () => import('./items/items.module').then(m => m.ItemsModule)
            }
            ];
            ```

    *  Opt-in usage sharing
    *  Angular Firebase
    *  Use of SVG as a template

**[⬆ Back to Top](#table-of-contents)**   |   <a href="#Q2">**⬆ Back to Question 2**</a>

----
  _Questions_ <a href="#Q1">**1**</a> | <a href="#Q2">**2**</a> | <a href="#Q3">**3**</a> | <a href="#Q4">**4**</a> | <a href="#Q5">**5**</a> | <a href="#Q6">**6**</a> | <a href="#Q7">**7**</a> | <a href="#Q8">**8**</a> | <a href="#Q9">**9**</a> | <a href="#Q10">**10**</a>
  ----

3. ### What are the building blocks of Angular?

    The Main Building blocks of Angular are
    *  Directives :

        * A directive modifies or manipulate the DOM by changing the appearance, behaviour or layout of DOM elements. Angular Directives are basically a **javaScript Class**.
        * There are 3 different directives:
          1. Component Directives
          2. Attribute Directives
          3. Structural Directives

    *  Modules : 

        *  Logical groupings of components, directives, services etc.

    *  Components :

        *  Basic building blocks of Angular.
        *  Made up of template, class and metadata.

    *  Meta Data :

        *  Tells Angular how to process a class. It is the information angular needs to decide if the particular class is a component, directive, service or just a regular class.
        * It is used to decorate a class using decorator.

    *  Templates : 

        *  UI/Views of an angular application; created using HTML.

    *  Data Binding : 

        *  Data binding is a core concept in Angular and allows to define communication between a component and the DOM, making it very easy to define interactive applications without worrying about pushing and pulling data. 
        *  There are four forms of data binding(divided as 3 categories) which differ in the way the data is flowing.
          
            1. **From the Component to the DOM:**

                1. **Interpolation:** {{ value }}: Adds the value of a property from the component
                    ```html
                    <li>Name: {{ user.name }}</li>
                    <li>Address: {{ user.address }}</li>
                    ```
                
                2. **Property binding:** [property]=”value”: The value is passed from the component to the specified property or simple HTML attribute
                    ```html
                    <input type="email" [value]="user.email">
                    ```
            2. **From the DOM to the Component:**
                
                1. **Event binding: (event)=”function”:** When a specific DOM event happens (eg.: click, change, keyup), call the specified method in the component
                    ```html
                    <button (click)="logout()"></button>
                    ```
            3. **Two-way binding:**
                
                1. **Two-way data binding:** [(ngModel)]=”value”: Two-way data binding allows to have the data flow both ways. For example, in the below code snippet, both the email DOM input and component email property are in sync
                    ```html
                    <input type="email" [(ngModel)]="user.email">
                    ```  

    *  Dependency Injection : 

        *  Dependency Injection is the technique in which classes receive thier dependencies from the external sources rathor than creating themselves.

    *  Services :

        *  Class with specific purpose.
        *  Used for sharing data, implementing application logic and interacting with external resoures.
        *  A service is used when a common functionality needs to be provided to various modules. Services allow for greater separation of concerns for your application and better modularity by allowing you to extract common functionality out of components.

    Let's create a repoService which can be used across components,

    ```typescript
    import { Injectable } from '@angular/core';
    import { Http } from '@angular/http';

    @Injectable({ // The Injectable decorator is required for dependency injection to work
      // providedIn option registers the service with a specific NgModule
      providedIn: 'root',  // This declares the service with the root app (AppModule)
    })
    export class RepoService{
      constructor(private http: Http){
      }

      fetchAll(){
        return this.http.get('https://api.github.com/repositories');
      }
    }
    ```
    The above service uses Http service as a dependency.  

**[⬆ Back to Top](#table-of-contents)**   |   <a href="#Q3">**⬆ Back to Question 3**</a>

----
  _Questions_ <a href="#Q1">**1**</a> | <a href="#Q2">**2**</a> | <a href="#Q3">**3**</a> | <a href="#Q4">**4**</a> | <a href="#Q5">**5**</a> | <a href="#Q6">**6**</a> | <a href="#Q7">**7**</a> | <a href="#Q8">**8**</a> | <a href="#Q9">**9**</a> | <a href="#Q10">**10**</a>
  ----


4. ### Which command is used to create service?

` ng gernerate service myservice `

The above command generates sleleton myservice class in

***_src/app/myservice.service.ts_***

**[⬆ Back to Top](#table-of-contents)**   |   <a href="#Q4">**⬆ Back to Question 4**</a>

----
  _Questions_ <a href="#Q1">**1**</a> | <a href="#Q2">**2**</a> | <a href="#Q3">**3**</a> | <a href="#Q4">**4**</a> | <a href="#Q5">**5**</a> | <a href="#Q6">**6**</a> | <a href="#Q7">**7**</a> | <a href="#Q8">**8**</a> | <a href="#Q9">**9**</a> | <a href="#Q10">**10**</a>
  ----


5. ### What is use of `ngIf` directive?

It is allows to add/remove the DOM element.

**[⬆ Back to Top](#table-of-contents)**   |   <a href="#Q4">**⬆ Back to Question 4**</a>