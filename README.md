# Angular-Cheat-Sheet
Certainly! Below is the Markdown file for the Angular Cheat Sheet covering various aspects of Angular development:


# Angular Cheat Sheet: Zero To Mastery

## Table of Contents

1. [Starting a New Project](#starting-a-new-project)
2. [Installing a Library](#installing-a-library)
3. [Creating Components](#creating-components)
4. [Lifecycle Hooks](#lifecycle-hooks)
5. [Services](#services)
6. [Modules](#modules)
7. [Angular Directives](#angular-directives)
8. [Pipes](#pipes)
9. [Decorators](#decorators)
10. [Angular Routing](#angular-routing)
11. [Angular HTTP Client](#angular-http-client)
12. [Angular Testing](#angular-testing)
13. [Useful Links](#useful-links)
    

---

## Starting a New Project

Before starting a new project, ensure that Node.js is installed on your machine. Angular provides an official CLI tool for managing projects, which can be installed via NPM or Yarn.

### Installation:

#### NPM:
```bash
npm install -g @angular/cli
```

#### Yarn:
```bash
yarn global add @angular/cli
```

### Creating a New Project:
```bash
ng new my-app
```

Angular will prompt you to configure the project. For default settings, press Enter/Return keys. During installation, Angular will scaffold a default project with necessary packages.

To run the project:
```bash
# Development
ng serve

# Production
ng build --prod
```

## Installing a Library

You may need to install 3rd-party libraries for your project. Angular provides a special command to install and configure Angular-optimized packages.

### Installation + Configuration:
```bash
ng add @angular/material
```

### Installation:
```bash
npm install @angular/material
```

---

## Creating Components

Components are the building blocks of an Angular application. They can be created using Angular CLI.

### Common:
```bash
ng generate component MyComponent
```

### Shorthand:
```bash
ng g c MyComponent
```

Angular will generate necessary files for the component in a directory with the same name.

---

## Lifecycle Hooks

Angular components emit events during and after initialization. Lifecycle hooks allow developers to hook into these events.

### Hooks:

- ngOnChanges
- ngOnInit
- ngDoCheck
- ngAfterContentInit
- ngAfterContentChecked
- ngAfterViewInit
- ngAfterViewChecked
- ngOnDestroy

---

## Services

Services are objects for outsourcing logic and data that can be injected into components. They are useful for reusing code across components.

### Creating a Service:

```bash
ng generate service MyService
```

---

## Modules

Angular enhances JavaScript's modularity with its own module system. Modules can register components, services, directives, and pipes.

### Example AppModule:
```typescript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppRoutingModule } from './app-routing.module';
import { AppComponent } from './app.component';

@NgModule({
  declarations: [AppComponent],
  imports: [BrowserModule, AppRoutingModule],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

---

## Angular Directives

Directives modify the behavior of elements and components in Angular applications. There are two types: attribute directives and structural directives.

### Attribute Directives:

- NgClass
- NgStyle
- NgModel

### Structural Directives:

- NgIf
- NgFor
- NgSwitch

## Creating Directives

Directives in Angular allow you to create custom HTML elements and attributes. They can be used to extend the behavior of existing DOM elements or create entirely new ones.

### Common Directives:

- **Attribute Directives:** These modify the behavior or appearance of an element.
- **Structural Directives:** These change the structure of the DOM by adding or removing elements.

### Creating a Directive:

```bash
ng generate directive MyDirective
```

---

## Pipes

Pipes transform content in templates without directly affecting data. Angular provides several built-in pipes.

### Examples:
- DatePipe
- UpperCasePipe
- LowerCasePipe
- CurrencyPipe
- DecimalPipe
- PercentPipe

---

## Decorators

Angular provides decorators that can be applied to classes and fields for various purposes.

### Common Decorators:
- @Input()
- @Output()
- @HostBinding()
- @HostListener()
- @ContentChild()
- @ContentChildren()
- @ViewChild()
- @ViewChildren()

---

## Angular Routing

Routing in Angular allows you to navigate between different components and views in your application without reloading the entire page. It helps in creating Single Page Applications (SPAs) where navigation occurs without page refresh.

### Setting Up Routing:

1. Define routes in the AppRoutingModule.
2. Import RouterModule and Routes from @angular/router.
3. Configure routes with path and component.
4. Add <router-outlet> in the template where the component will be rendered.

Example:
```typescript
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { HomeComponent } from './home.component';
import { AboutComponent } from './about.component';

const routes: Routes = [
  { path: 'home', component: HomeComponent },
  { path: 'about', component: AboutComponent }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

---

## Angular Forms

Angular provides powerful tools for handling forms, including template-driven forms and reactive forms.

### Template-driven Forms:

Template-driven forms are easy to use and suitable for simple forms with less logic.

### Reactive Forms:

Reactive forms provide a more flexible and scalable approach to handling forms. They are more suitable for complex forms with dynamic behavior.

---

## Angular HTTP Client

Angular provides a built-in HTTP client module for making HTTP requests to servers.

### Usage:

1. Import the HttpClientModule.
2. Inject the HttpClient service into your component or service.
3. Use HttpClient methods like get(), post(), put(), delete(), etc., to make HTTP requests.

Example:
```typescript
import { HttpClient } from '@angular/common/http';

@Injectable({
  providedIn: 'root'
})
export class DataService {
  constructor(private http: HttpClient) { }

  getData() {
    return this.http.get('/api/data');
  }
}
```

---

## Angular Testing

Angular provides tools and utilities for testing your application's components, services, and other features.

### Types of Testing:

1. **Unit Testing:** Testing individual components or services in isolation.
2. **Integration Testing:** Testing how components or services work together.
3. **End-to-End Testing:** Testing the entire application flow from start to finish.

### Tools:

- Jasmine: A behavior-driven development framework for testing JavaScript code.
- Karma: A test runner for executing unit tests.
- Protractor: An end-to-end testing framework for Angular applications.

---

**Back To Top**


## Useful Links

- [Angular Documentation](https://angular.io/docs)
- [Angular Devtools](https://angular.io/guide/devtools)
- [Angular API Reference](https://angular.io/api)
- [Angular Blog](https://blog.angular.io/)
- [Angular Routing](https://angular.io/guide/router)
- [Angular Forms](https://angular.io/guide/forms)

---


 Let me know if you need further modifications or any mistakes.
