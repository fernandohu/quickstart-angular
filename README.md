# Angular Quickstart

Project startup with Angular 8 and Docker. 

By leveraging the power of Docker you don't need to install Node JS or Angular Cli in your computer. You just run everything from a Docker container.

## Requirements

- Git;
- Docker;
- Docker Compose.

## Installation

1) Clone the repository:

```
git clone git@github.com:fernandohu/quickstart-angular.git
```

2) Use Docker to run `npm install` on the angular source code at `app/` folder:

```
docker-compose run --rm angular npm install
```

3) Run `docker compose` to start up the development environment:

```
docker-compose up
```

After running `docker-compose up` the application should be accessible at http://localhost:4200.

## Developing

The source code resides at `/app`. Every time you change a file inside this folder, the browser will be automatically updated with the new content (thanks to Webpack). 

The files were generated with `ng create`. If you wish, you can remove everything in this folder and regenerate it by your way.

## Executing ng or npm 

You can execute `ng` or `npm` commands by calling the `angular` service:

```
docker-compose run --rm angular npm XXX
```

or

```
docker-compose run --rm angular ng XXX
```

The commands will be always executed in the `app` folder.

## Connect to the container

```
docker exec -it angular-cli bash
```
