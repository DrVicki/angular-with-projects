# Chapter 1: Creating Your First Web Application in Angular 

Angular is a popular and modern JavaScript framework that can run on different platforms additional to the web, such as desktop and mobile. 
Angular applications are written in TypeScript, a superset of JavaScript that provides syntactic sugar such as strong typing and object-oriented 
techniques. Angular applications are created and developed using a command-line tool made by the Angular team called the Angular CLI. It 
automates many development tasks, such as scaffolding, testing, and deploying an Angular application, which would take a lot of time to configure 
manually. The popularity of the Angular framework is considerably reflected in its broad support of tooling. The Visual Studio Code (VSCode) editor 
contains various extensions that enhance the development experience when working with Angular. In this chapter, we will cover the following topics: 

  - Introduction to Angular 
  - Introduction to the Angular CLI Exploring the rich ecosystem of Angular tooling in VSCode How to create our first Angular application  
  - How to use Nx Console for automating Angular CLI commands

## Essential background theory and context 

The Angular framework is a cross-platform JavaScript framework that can run on a wide range of environments, including the web, servers, mobile, and desktop. 
It consists of a collection of JavaScript libraries that we can use for building highly performant and scalable web applications. The architecture of an Angular 
application is based on a hierarchical representation of components. Components are the fundamental building blocks of an Angular application. They represent 
and control a particular portion of a web page called the view. 

Some examples of components are as follows: 

  - A list of blog posts 
  - An issue reporting form 
  - A weather display widget 

Components of an Angular application can be logically organized as a tree: Figure 1.1 – Component tree 

An Angular application typically has one main component, called ```AppComponent```, by convention. Each component 
in the tree can communicate and interact with its siblings using an application programming interface defined by 
each one. An Angular application can have many features called modules. Each module serves a block of single 
functionality that corresponds to a particular application domain or workflow. Angular modules are used to group 
Angular components that share similar functionality: 

Figure 1.2 – Module hierarchy 

In the previous diagram, the dashed line circles represent Angular modules. An Angular application typically has one 
main module, called ```AppModule```, by convention. Each module can import other modules in an Angular application if 
they wish to use part of their functionality. The functionality of a module can be further analyzed in the 
presentational and business logic of a feature. Angular components should only be responsible for handling the presentational 
logic and delegating business logic tasks to services. The Angular framework provides Angular services to components using a 
built-in dependency injection (DI) mechanism. The Angular DI framework uses special-purpose objects, called injectors, to hide 
much of the complexity of providing dependencies to an Angular application. Components are not required to know any of the actual 
implementation of an Angular service. They only need to ask for it from an injector. An Angular service should follow the single 
responsibility principle, and it should not cross boundaries between different Angular modules. 

Some examples of services are as follows: 
  - Access data from a backend API using the HTTP protocol. 
  - Interact with the local storage of the browser. 
  - Error logging. 
  - Data transformations. 

An Angular developer does not need to remember how to create components, 
modules, and services by heart while building an Angular application. 
Luckily, the Angular CLI can assist us by providing a command-line 
interface to accomplish these tasks. 

## Introduction to the Angular CLI 

The Angular CLI is a tool created by the Angular team that improves the 
developer experience while building Angular applications. It hides much of 
the complexity of scaffolding and configuring an Angular application while 
allowing the developer to concentrate on what they do best – coding! 

Before we can start using the Angular CLI, we need to set up the following 
prerequisites in our system: 

  - Node.js: A JavaScript runtime built on the v8 engine of Chrome. You can 
download any Long-Term Support (LTS) version from https://nodejs.org/en. 

  - npm: A package manager for the Node.js runtime. We can then install the 
Angular CLI using ```npm``` from the command line: 

```npm install -g @angular/cli``` 

We can use the ```-g``` option to install the Angular CLI globally since we 
want to create Angular applications from any path of our operating system. 

Important note 
Installing the Angular CLI may require administrative privileges in some operating 
systems. To verify the Angular CLI has been installed correctly, we can run the 
following from the command line: 

```ng version``` 

The previous command will report the version of the Angular CLI installed in our system. 
The Angular CLI provides a command-line interface through the ng command, which is the 
binary executable of the Angular CLI. It can accept various options, including the following: 

  - **serve**: Build and serve an Angular application. 
  - **build**: Build an Angular application. 
  - **test**: Run the unit tests of an Angular application. 
  - **generate**: Generate a new Angular artifact, such as a component or module. 
  - **add**: Install a third-party library compatible with the Angular framework. 
  - **new**: Create a new Angular application.

The previous options are the most common ones. If you want to view all the available commands, execute the following in the command line: 

```ng help``` 

The previous command will display a list of all the supported commands from the Angular CLI. 

The Angular tooling ecosystem is full of extensions and utilities which can help us when developing Angular applications. In the next section, we will overview some which work with VSCode. 

## Angular tooling in VSCode

There are many extensions available in the VSCode Marketplace to enhance the Angular tooling ecosystem. In this section, we will learn about the most popular ones which can significantly help us in Angular development: 

  - Nx Console 
  - Angular Language Service 
  - Angular Snippets 
  - Angular Evergreen 
  - Material Icon Theme 
  
  
The preceding list is not exhaustive, and some of the extensions are already included in the Angular Essentials pack. However, you can browse more Angular extensions for ![VSCode](https://marketplace.visualstudio.com/search?term=angular&target=VSCode).  

### Nx Console 

The Nx Console is a VSCode extension developed by the Nrwl team which provides a graphical user interface over the Angular CLI. 
  - It contains most of the Angular CLI commands, and it uses the Angular CLI internally to execute each one. 

We will learn more about this extension in the Building our application with Nx Console section. 

### Angular Language Service 

The Angular Language Service extension provides various enhancements while editing HTML templates in an Angular application, including the following: 
  - Code autocompletion 
  - Compile error messages 
  - Go-to definition techniques 

Code autocompletion is a feature which helps us find the right property or method to use while typing. 
  - It works by displaying a list of suggestions while we start typing in HTML content:

Figure 1.3 – Code completion 

In the previous screenshot, when we start typing the word **ti**, the Angular Language Service suggests the title component property. 
  - Notice code completion only works for the public properties and methods in a component. 

One of the most common issues when developing web applications is detecting errors before the application reaches production. 
  - This problem can be solved partially by the Angular compiler, which is bootstrapped upon building an Angular application for production. 
  - Moreover, the Angular Language Service can take this further by displaying compilation error messages far before our application reaches the compilation process:

Figure 1.4 – Compile error message 

For example, if we accidentally misspell the name of a property or method of the component, the Angular Language Service will display an appropriate error message. 

### Angular Snippets 

The Angular Snippets extension contains a collection of Angular code snippets for TypeScript and HTML. 
  - In TypeScript, we can use it to create components, modules, or services in a blank TypeScript file:

Figure 1.5 – New Angular component snippet 

In an HTML template, we can use the extension to create useful Angular artifacts, such as the ```*ngFor``` directive, to loop through a list in HTML: 

Figure 1.6 – *ngFor snippet 

Due to the widespread popularity and capabilities of the Angular CLI, it looks more convenient to use it for generating Angular artifacts in TypeScript. However, Angular Snippets does a great job with the HTML part, where there are more things to remember. Angular Evergreen One of the primary factors that makes the Angular framework so stable is that it follows a regular release cycle based on semantic versioning. If we want our Angular applications to be packed with the latest features and fixes, we must update them regularly. But how can we stay up to date in the most efficient way? We can use the Angular Evergreen extension for that! It compares the Angular and Angular CLI versions of an Angular CLI project with the latest ones and alerts you about whether you need to update it:

Bampakos, Aristeidis. Angular Projects: Build modern web apps by exploring Angular 12 with 10 different projects and cutting-edge technologies, 2nd Edition . Packt Publishing. Kindle Edition. 

  
