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
in the tree can communicate and interact with its siblings
