# Vuejs3-Docker
A simple HelloWorld Vuejs 3 project in Docker container

## To start the project with image building

```sh
docker compose up --build
```

## To start the project without building

```sh
docker compose up
```

Basically, it will install all the js dependencies and start a dev server at

```
http://localhost:3000/
```

## The projet has the following dependencies:
```
✔ Project name: … frontend
✔ TypeScript? …  Yes
✔ JSX Support? … No
✔ Vue Router for Single Page Application development? … Yes
✔ Pinia for state management? … Yes
✔ Vitest for Unit testing? … No
✔ Cypress for both Unit and End-to-End testing? … No
✔ ESLint for code quality? … Yes
✔ Prettier for code formatting? … Yes
```
## You can add/remove dependencies at your convenience whith the command:
```sh
docker exec -ti vuejs3-frontend npm install <dependency name>
```
OR
```sh
docker exec -ti vuejs3-frontend npm uninstall <dependency name>
```
ALTERNATIVELY, modify the package.json file at your convenience, then:
```sh
docker exec -ti vuejs3-frontend npm install
```


## You can access the container with:
```sh
docker exec -ti vuejs3-frontend /bin/sh
```
