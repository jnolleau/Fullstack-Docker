# Fullstack-Docker
A fullstack docker starter kit with Vue.js 3, Nestjs, PostgreSQL and adminer

## Application structure:
- [Vue.js 3](https://v3.vuejs.org/guide/introduction.html) as frontend accessible at http://localhost:8080
- [NestJS](https://docs.nestjs.com/) as backend accessible at http://localhost:3000
- a database [PostgreSQL](https://www.postgresql.org/docs/13/index.html)
- [Adminer](https://www.adminer.org/en/) as database management tool accessible at http://localhost:8000

## To start the project with image building
It basically creates a .env file and launch docker compose with --build tag

```sh
./setup.sh
```

## To start the project without building
Not suitable is no .env and no built image exist
```sh
docker compose up
```

Basically, it will install all the js dependencies and start a dev server at

```
http://localhost:00/
```

## The Vue,js frontend has the following dependencies:
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

## You can access containers with:
### Frontend
```sh
docker exec -ti vuejs3-frontend /bin/sh
```
### Backend
```sh
docker exec -ti nestjs-backend /bin/sh
```
