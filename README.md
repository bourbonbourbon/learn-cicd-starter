![code coverage badge](https://github.com/bourbonbourbon/learn-cicd-starter/actions/workflows/ci.yml/badge.svg)

# learn-cicd-starter (Notely)

This repo contains the starter code for the "Notely" application for the "Learn CICD" course on [Boot.dev](https://boot.dev).

## PlanetScale unavailable in country workaround
1. Create a Cloud SQL instance, name it whatever.
2. Create a database in that instance called notely-db.
3. `DATABASE_URL` format will be `USER:PASSWORD@tcp(IP)/DATABASE_NAME`.
4. Run `migrateup.sh`.
5. Add `DATABASE_URL` to Github Secrets and Secrets Manager on GCP.

> Note: Check out [env.md](./env.md) for more information.

## Local Development

Make sure you're on Go version 1.20+.

Create a `.env` file in the root of the project with the following contents:

```bash
PORT="8080"
```

Run the server:

```bash
go build -o notely && ./notely
```

_This starts the server in non-database mode._ It will serve a simple webpage at `http://localhost:8080`.

You do _not_ need to set up a database or any interactivity on the webpage yet. Instructions for that will come later in the course!
