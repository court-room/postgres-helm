postgres-helm
=============

## Setup
In order to use this chart you have to create a secret with the name `postgres-secret`,
containing the following variable `POSTGRES_PASSWORD`.
This is a required setup and the release won't work without this.
```bash
$ helm repo add postgres https://court-room.github.io/postgres-helm
$ helm repo update
$ helm install my-postgres-helm postgres/postgres-helm
```

## TODO
1. Fix test cases for helm chart
