# Angular-8 Interview Questions & Answers

> Click :star:if you like the project. Pull Request are highly appreciated.

### Table of Contents

| No. | Questions |
|---- | ---------
| <span id="Q1">1</span> | [What is Angular 8?](#what-is-angular-8)|
| <span id="Q2">2</span> | [What is new in Angular 8?](#what-is-new-in-angular-8)|
| <span id="Q3">3</span> | [What are the building blocks of Angular?](#what-are-the-building-blocks-of-angular)|
| <span id="Q4">4</span> | [Which command is used to create service?](#Which-command-is-used-to-create-service)|

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

    *  Support for Bazel :

        *  Bazel is build tool developed and used by Google.
        *  The angluar community is working to integrate Bazel tool in to the standard angular toolset to enable developers to perform faster builds on large projects.
        *  It allows to deploy only what has been changed.
        *  Opt-in Option with Angular 8.

    *  Support for Web Worker Bundling
    *  New changes in ViewChild and ContentChild
    *  Builder API and Workspace APIs in the CLI
    *  Differential Loading by Default : 
        
        *  Creates two bundles which will be loaded according to the browser version and support : 
            1. ES6+ Bundle - For New browsers support; So that new browser loads less code to run the app in the browser.
            2. ES5 Bundle - For Old browsers support; So that old browser loads more code to run the app in the browser.

    *  Improvements in AngularJS Migration
    *  Lazy Loading with Dynamics Imports :

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

    *  Modules
    *  Components
    *  Meta Data
    *  Templates
    *  Data Binding
    *  Dependency Injection
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