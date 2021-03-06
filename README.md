# golangspell

Golang Spell is a productivity platform for building Microservices using Golang

Golang Spell makes it possible to build lightning fast Microservices in Go 
in an easy and productive way.
Welcome to the platform that will kick out the boilerplate code 
and drive you through new amazing possibilities

## Dependency Management

The project is using [Go Modules](https://blog.golang.org/using-go-modules) for dependency management
Module: github.com/danilovalente/golangspell

## Architectural Model

The Architectural Model adopted to structure the applications created with Golang Spell is based on The Clean Architecture.
Further details can be found here: [The Clean Architecture](https://8thlight.com/blog/uncle-bob/2012/08/13/the-clean-architecture.html) and in the Clean Architecture Book.

## Package Structure

Following the Clean Architecture principles, the generated applications will be structured in accordance with the following package structure:

* `root package:` Main package, containing all the inner application packages. Defined like the AppName provided during the project initialization (init command)
* `appcontext:` Application context with the core Component Management features needed to make it possible to provide a basic [Dependency Injection](https://www.martinfowler.com/articles/injection.html) mechanism
* `config:` Configuration of the application environment
* `controller:` Contains the REST controllers from the application.
* `domain:` Contains all the domain entities.
* `gateway:` Adapters/Clients for the external resources, like databases, streams, queues, http, cache...
* `usecase:` Contains the implementation of the use cases which the application is supposed to provide.

## Instalation

Run the following command to install the tool in your GOPATH:

```bash
go get github.com/danilovalente/golangspell
```

Add to your O.S. the following Path:

```bash
$GOPATH/bin
```

## Usage

The command **golangspell help** shows all available options.  
To start a new project, the starting point is the command init (to know more run **golangspell help init**)

![Spell Gopher](http://derobgfa8qo3s.cloudfront.net/images/gopher_spell.png)

## Version History
* 0.3.6 Fixed version tracking
* 0.3.5 Added (minor) feature for getting the current module and adjusted render
* 0.3.4 Template to string adjusted
* 0.3.3 Template to string adjusted
* 0.3.2 Added template to string (minor) feature in the renderer, lint checked and code adjusted
* 0.3.1 Exposed Backup feature in the renderer