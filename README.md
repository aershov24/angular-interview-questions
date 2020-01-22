# Angular Interview Questions and Answers

The Angular 9 RC is out, what an exciting time to be Angular developer. Ivy is here, Ivy is now the default rendering engine in Angular. Follow along and check latest Angular X Interview Questions and Answers with latest Ivy updates for 2020.

> You could also find all the answers here 👉 https://www.fullstack.cafe/Angular.

## Q1: What is Routing Guard in Angular? ⭐

**Answer:**

Angular’s route guards are interfaces which can tell the router whether or not it should allow navigation to a requested route. They make this decision by looking for a true or false return value from a class which implements the given guard interface.

🔗 **Source:** [medium.com](https://medium.com/@ryanchenkie_40935/angular-authentication-using-route-guards-bf7a4ca13ae3)


## Q2: What is a module, and what does it contain? ⭐

**Answer:**

An Angular module is set of Angular basic building blocks like component, directives, services etc. An app can have more than one module.

A module can be created using `@NgModule` decorator.

```js
@NgModule({
  imports:      [ BrowserModule ],
  declarations: [ AppComponent ],
  bootstrap:    [ AppComponent ]
})
export class AppModule { }
```

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/40073941/whats-the-difference-between-an-angular-component-and-module)


## Q3: What are pipes? Give me an example. ⭐

**Answer:**

A **pipe** takes in data as input and transforms it to a desired output. You can chain pipes together in potentially useful combinations. You can write your own custom pipes. Angular comes with a stock of pipes such as `DatePipe`, `UpperCasePipe`, `LowerCasePipe`, `CurrencyPipe`, and `PercentPipe`.

Consider:
```html
<p>The hero's birthday is {{ birthday | date }}</p>
```
In this page, you'll use pipes to transform a component's birthday property into a human-friendly date.

🔗 **Source:** [angular.io](https://angular.io/guide/pipes)


## Q4: What are the differences between AngularJS (angular 1.x) and Angular (Angular 2.x and beyond)? ⭐⭐

**Answer:**

Angular and AngularJS is basically a different framework with the same name.

Angular is more ready for the current state of web standards and the future state of the web (ES6\7, immutiablity, components, shadow DOM, service workers, mobile compatibilty, modules, typescript and so on and so on... )

Angular killed many main features in AngularJS like - controllers, $scope, directives (replaced with `@component` annotations), the module definition, and much more, even simple things like ng-repeat has not left the same as it was.

Also: 
1. They added an angular `cli`.
2. Your angular code is written in ES6 Typescript and it compiles at runtime to Javascript in the browser.
3. You bind to your HTML similarly like how you would if in an Angular 1 directive. So variable like $scope and $rootScope have been deprecated.

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/34114593/angular-vs-angular-2)


## Q5: What is a component? Why would you use it? ⭐⭐

**Answer:**

*Components* are the most basic building block of an UI in an Angular application. An Angular application is a tree of Angular components. Angular components are a subset of directives. Unlike directives, components always have a template and only one component can be instantiated per an element in a template.

A component must belong to an NgModule in order for it to be usable by another component or application. To specify that a component is a member of an NgModule, you should list it in the `declarations` field of that NgModule.

```js
@Component({selector: 'greet', template: 'Hello {{name}}!'})
class Greet {
  name: string = 'World';
}
```

🔗 **Source:** [angular.io](https://angular.io/api/core/Component)


## Q6: What is the minimum definition of a component? ⭐⭐

**Answer:**

The absolute minimal configuration for a `@Component` in Angular is a template. Both template properties are set to optional because you have to define either `template` or `templateUrl`.

When you don't define them, you will get an exception like this:
```sh
No template specified for component 'ComponentName'
```
A selector property is not required, as you can also use your components in a route.

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/46338698/minimum-definition-of-a-component-angular-4)


## Q7: What's the difference between an Angular component and module? ⭐⭐

**Answer:**

*Components* control views (html). They also communicate with other components and services to bring functionality to your app.

*Modules* consist of one or more components. They do not control any html. Your modules declare which components can be used by components belonging to other modules, which classes will be injected by the dependency injector and which component gets bootstrapped. Modules allow you to manage your components to bring modularity to your app.

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/40073941/whats-the-difference-between-an-angular-component-and-module)


## Q8: What is a service, and when will you use it? ⭐⭐

**Answer:**

*Angular services* are singleton objects which get instantiated only once during the lifetime of an application. They contain methods that maintain data throughout the life of an application, i.e. data does not get refreshed and is available all the time. The main objective of a service is to organize and share business logic, models, or data and functions with different components of an Angular application.

The *separation of concerns* is the main reason why Angular services came into existence. An Angular service is a stateless object and provides some very useful functions. 

🔗 **Source:** [dzone.com](https://dzone.com/articles/what-is-a-service-in-angular-js-why-to-use-it)


## Q9: What is the equivalent of ngShow and ngHide in Angular? ⭐⭐

**Answer:**

Just bind to the `hidden` property

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/35578083)


## Q10: You have an HTML response I want to display. How do I do that?  ⭐⭐

**Answer:**

The correct syntax is the following:
```html
<div [innerHTML]="theHtmlString"></div>
```
Working in `5.2.6`

🔗 **Source:** [medium.com](https://medium.com/wizardnet972/48-answers-on-stack-overflow-to-the-most-popular-angular-questions-52f9eb430ab0)


## Q11: How can I select an element in a component template? ⭐⭐

**Answer:**

You can get a handle to the DOM element via ElementRef by injecting it into your component's constructor:

```js
constructor(myElement: ElementRef) { ... }
```

🔗 **Source:** [medium.com](https://medium.com/wizardnet972/48-answers-on-stack-overflow-to-the-most-popular-angular-questions-52f9eb430ab0)


## Q12: What is the equivalent of "ngShow" and "ngHide" in Angular? ⭐⭐

**Answer:**

Just bind to the hidden property:

```js
[hidden]="!myVar"
```

🔗 **Source:** [medium.com](https://medium.com/wizardnet972/48-answers-on-stack-overflow-to-the-most-popular-angular-questions-52f9eb430ab0)


## Q13: What is the difference between *ngIf vs [hidden]? ⭐⭐

**Answer:**

`*ngIf` effectively removes its content from the DOM while `[hidden]` modifies the `display` property and only instructs the browser to not show the content but the DOM still contains it.

🔗 **Source:** [medium.com](https://medium.com/wizardnet972/48-answers-on-stack-overflow-to-the-most-popular-angular-questions-52f9eb430ab0)


## Q14: What is the difference between "@Component" and "@Directive" in Angular?  ⭐⭐

**Answer:**

* **Directives** add behaviour to an existing DOM element or an existing component instance.
* **A component**, rather than adding/modifying behaviour, actually creates its own view (hierarchy of DOM elements) with attached behaviour.

Write a component when you want to create a reusable set of DOM elements of UI with custom behaviour. Write a directive when you want to write reusable behaviour to supplement existing DOM elements.

🔗 **Source:** [medium.com](https://medium.com/wizardnet972/48-answers-on-stack-overflow-to-the-most-popular-angular-questions-52f9eb430ab0)


## Q15: What does this line do? ⭐⭐

**Questions Details:**

```js
@HostBinding('[class.valid]') isValid;
```


**Answer:**

`@HostBinding` lets you set properties on the element or component that hosts the directive.

The code applies the css class `valid` to whatever is using this directive conditionally based on the value of isValid.

🔗 **Source:** [alligator.io](https://alligator.io/angular/hostbinding-hostlistener/)


## Q16: How would you protect a component being activated through the router? ⭐⭐

**Answer:**

The Angular router ships with a feature called guards. These provide us with ways to control the flow of our application. We can stop a user from visitng certain routes, stop a user from leaving routes, and more. The overall process for protecting Angular routes:

* Create a guard service: `ng g guard auth`
* Create `canActivate()` or `canActivateChild()` methods
* Use the guard when defining routes

```js
// import the newly created AuthGuard
const routes: Routes = [
  {
    path: 'account',
    canActivate: [AuthGuard]
  }
];
```

Some other available guards:

* `CanActivate`: Check if a user has access
* `CanActivateChild`: Check if a user has access to any of the child routes
* `CanDeactivate`: Can a user leave a page? For example, they haven't finished editing a post
* `Resolve`: Grab data before the route is instantiated
* `CanLoad`: Check to see if we can load the routes assets

🔗 **Source:** [scotch.io](https://scotch.io/tutorials/protecting-angular-v2-routes-with-canactivatecanactivatechild-guards)


## Q17: What are some differences between Angular 2 and 4? ⭐⭐

**Answer:**

Just to name a few:
* Improvements in AOT, 
* allowing the "else" clause in ngIf, 
* support for TypeScript 2.1
* breaking out the animations package

🔗 **Source:** [github.com/WebPredict](https://github.com/WebPredict/angular-2-interview-questions)


## Q18: How would you run unit test? ⭐⭐

**Answer:**

The Angular CLI downloads and install everything you need to test an Angular application with the Jasmine test framework.

The project you create with the CLI is immediately ready to test. Just run this one CLI command:

```sh
ng test
```

🔗 **Source:** [angular.io](https://angular.io/guide/testing)


## Q19: What is the difference between Structural and Attribute directives in Angular? ⭐⭐

**Answer:**

* **Structural directives** are used to alter the DOM layout by removing and adding DOM elements. It is far better in changing the structure of the view. Examples of Structural directives are NgFor and Nglf.

* **Attribute Directives** These are being used as characteristics of elements. For example, a directive such as built-in NgStyle in the template Syntax guide is an attribute directive.

🔗 **Source:** [onlineinterviewquestions.com](https://www.onlineinterviewquestions.com/angular-7-interview-questions/)


## Q20: What is the purpose of base href tag? ⭐⭐

**Answer:**

The routing application should add <base> element to the index.html as the first child in the <head> tag inorder to indicate how to compose navigation URLs. If app folder is the application root then you can set the href value as below
```html
    <base href="/">
```

🔗 **Source:** [github.com/sudheerj](https://github.com/sudheerj/angular-interview-questions/blob/master/README.md)


## Q21: What is an observer? ⭐⭐

**Answer:**

Observer is an interface for a consumer of push-based notifications delivered by an Observable. It has below structure,
```javascript
    interface Observer<T> {
      closed?: boolean;
      next: (value: T) => void;
      error: (err: any) => void;
      complete: () => void;
    }
```
A handler that implements the Observer interface for receiving observable notifications will be passed as a parameter for observable as below,
```javascript
    myObservable.subscribe(myObserver);
```
**Note:** If you don't supply a handler for a notification type, the observer ignores notifications of that type.

🔗 **Source:** [github.com/sudheerj](https://github.com/sudheerj/angular-interview-questions/blob/master/README.md)


## Q22: What is an observable? ⭐⭐

**Answer:**

 An Observable is a unique Object similar to a Promise that can help manage async code. Observables are not part of the JavaScript language so we need to rely on a popular Observable library called RxJS.
    The observables are created using new keyword. Let see the simple example of observable,
```javascript
    import { Observable } from 'rxjs';

    const observable = new Observable(observer => {
      setTimeout(() => {
        observer.next('Hello from a Observable!');
      }, 2000);
    });`
```

🔗 **Source:** [github.com/sudheerj](https://github.com/sudheerj/angular-interview-questions/blob/master/README.md)


## Q23: What are observables? ⭐⭐

**Answer:**

**Observables** are declarative which provide support for passing messages between publishers and subscribers in your application. They are mainly used for event handling, asynchronous programming, and handling multiple values. In this case, you define a function for publishing values, but it is not executed until a consumer subscribes to it. The subscribed consumer then receives notifications until the function completes, or until they unsubscribe.

🔗 **Source:** [github.com/sudheerj](https://github.com/sudheerj/angular-interview-questions/blob/master/README.md)


## Q24: What is a bootstrapping module? ⭐⭐

**Answer:**

Every application has at least one Angular module, the root module that you bootstrap to launch the application is called as bootstrapping module. It is commonly known as AppModule. The default structure of AppModule generated by AngularCLI would be as follows,
```javascript
    /* JavaScript imports */
    import { BrowserModule } from '@angular/platform-browser';
    import { NgModule } from '@angular/core';
    import { FormsModule } from '@angular/forms';
    import { HttpClientModule } from '@angular/common/http';

    import { AppComponent } from './app.component';

    /* the AppModule class with the @NgModule decorator */
    @NgModule({
      declarations: [
        AppComponent
      ],
      imports: [
        BrowserModule,
        FormsModule,
        HttpClientModule
      ],
      providers: [],
      bootstrap: [AppComponent]
    })
    export class AppModule { }
```

🔗 **Source:** [github.com/sudheerj](https://github.com/sudheerj/angular-interview-questions/blob/master/README.md)


## Q25: What is interpolation? ⭐⭐

**Answer:**

**Interpolation** is a special syntax that Angular converts into property binding. It’s a convenient alternative to property binding. It is represented by double curly braces({{}}). The text between the braces is often the name of a component property. Angular replaces that name with the string value of the corresponding component property.
Let's take an example,
```html
    <h3>
      {{title}}
      <img src="{{url}}" style="height:30px">
    </h3>
```
In the example above, Angular evaluates the title and url properties and fills in the blanks, first displaying a bold application title and then a URL.

🔗 **Source:** [github.com/sudheerj](https://github.com/sudheerj/angular-interview-questions/blob/master/README.md)


## Q26:  Explain the difference between `Promise` and `Observable` in Angular? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q27: Explain the difference between "Constructor" and "ngOnInit" ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q28: What is the difference between `@Component` and `@Directive` in Angular? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q29: Can you explain the difference between `Promise` and `Observable` in Angular? In what scenario can we use each case? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q30: Why should `ngOnInit` be used, if we already have a `constructor`? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q31: How to bundle an Angular app for production? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q32: What is difference between "declarations", "providers" and "import" in NgModule? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q33: What is Reactive Programming and how to use one with Angular? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q34: What's new in Angular 6 and why shall we upgrade to it? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q35: Why would you use a spy in a test? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q36: What is TestBed? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q37: What is Protractor? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q38: What is the point of calling "renderer.invokeElementMethod(rendererEl, methodName)"? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q39: How would you control size of an element on resize of the window in a component? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q40: What is AOT? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q41: What is Redux and how does it relate to an Angular app? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q42: What is the use of codelyzer? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q43: How to inject base href? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q44: When would you use eager module loading? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q45: What are the Core Dependencies of Angular 7? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q46: Why Incremental DOM Has Low Memory Footprint? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q47: What are the ways to control AOT compilation? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q48: What is Angular Universal? ⭐⭐⭐

**Questions Details:**

Angular Universal is a server-side rendering module for Angular applications in various scenarios. This is a community driven project and available under`@angular/platform-server` package. Recently Angular Universal is integrated with Angular CLI.


 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q49: Do I need a Routing Module always? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q50: What is the purpose of Wildcard route? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q51: What is activated route? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q52: What is router state? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q53: What is router outlet? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q54: What are dynamic components? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q55: Explain how custom elements works internally? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q56: What are custom elements? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q57: What are the utility functions provided by RxJS? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q58: How do you perform error handling in observables? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q59: What is multicasting? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q60: What is the difference between promise and observable? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q61: What is subscribing? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q62: How do you perform Error handling for HttpClient? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q63: What is a parameterized pipe? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q64: How do you categorize data binding types? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q65: What happens if you use script tag inside template? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q66: What is the option to choose between inline and external template file? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q67: What's new in Angular 8? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q68: Angular 8: What is Bazel? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q69: Angular 8: What is Angular Ivy? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q70: Angular 8: Explain Lazy Loading in Angular 8? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q71: What are the lifecycle hooks for components and directives? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q72: When should I store the "Subscription" instances and invoke `unsubscribe()` during the NgOnDestroy life cycle and when can I simply ignore them? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q73: Could I use jQuery with Angular? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q74: How to set headers for every request in Angular? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q75: How to detect a route change in Angular? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q76: What is the need for SystemJS in Angular? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q77: Are there any pros/cons (especially performance-wise) in using local storage to replace cookie functionality? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q78: What does "detectChanges" do in Angular jasmine tests? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q79: Why would you use renderer methods instead of using native element methods? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q80: What would be a good use for NgZone service? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q81: What is Zone in Angular? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q82: How would you insert an embedded view from a prepared TemplateRef? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q83: What does a just-in-time (JIT) compiler do (in general)? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q84: What is Reactive programming and how does it relate to Angular? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q85: Name some security best practices in Angular ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q86: What is ngUpgrage?  ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q87: How do you create application to use scss? What changed for Angular 6? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q88: Name and explain some Angular Module Loading examples ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q89: Why would you use lazy loading modules in Angular app? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q90: When does a lazy loaded module is loaded? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q91: What is Ivy Renderer? Is it supported by Angular 7? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q92: What is incremental DOM? How is it different from virtual DOM? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q93: Why do we need compilation process? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q94: What are the advantages with AOT? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q95: What are the mapping rules between Angular component and custom element? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q96: Do I need to bootstrap custom elements? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q97: What is the difference between pure and impure pipe? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q98: Angular 8: Why we should use Bazel for Angular builds? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q99: Explain the purpose of Service Workers in Angular ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q100: Angular 9: What are some new features in Angular 9? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q101: What is the difference between BehaviorSubject vs Observable? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q102: What is the Angular equivalent to an AngularJS "$watch"? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q103: Is there no equivalent to `$scope.emit()` or `$scope.broadcast()` in Angular? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q104: Name some differences between SystemJS vs WebPack? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q105: Could you provide some particular examples of using ngZone? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q106: What is the default compilation for Angular 5? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q107: Just-in-Time (JiT) vs Ahead-of-Time (AoT) compilation. Explain the difference. ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q108: Do you know how you can run angularJS and angular side by side? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q109: How would you extract webpack config from angular cli project? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q110: Why angular uses url segment? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q111: When to use query parameters versus matrix parameters? ⭐⭐⭐⭐⭐

**Questions Details:**

* Query parameters: http://example.com/apples?order=random&color=blue
* Matrix parameters: http://example.com/apples;order=random;color=blue


 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q112: Why did the Google team go with incremental DOM instead of virtual DOM? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q113: Why Incremental DOM is Tree Shakable? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q114: What's new in Angular 7? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q115: What are observable creation functions? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q116: Angular 8: How does Ivy affect the (Re)build time? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q117: Angular 8: What are some changes in Location module? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q118: Angular 9: What is Locality principle for Ivy? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q119: Angular 9: Explain improvements in Tree-Shaking ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**


## Q120: Angular 9: How Would You Compare View Engine vs Ivy? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/Angular)**





