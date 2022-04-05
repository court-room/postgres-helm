postgres-helm
=============

## Setup
In order to use this chart you have to create a secret with the name `postgres-secret`,
containing the following variable `POSTGRES_PASSWORD`.
This is a required setup and the release won't work without this.
<!-- ```bash
helm repo add postgres https://court-room.github.io/postgres-helm
helm repo update
``` -->
You can install this repo by cloning the source and then installing as a local chart
```bash
helm install psotgres chart/postgres
```

## Configuration
You can provide the following configs for the Postgres Deployment

|Config|Description|Default|
|:---|:---|:---|
|`config.POSTGRES_DB`|Default database name to be created|`postgres`|
|`config.POSTGRES_USER`|Default database user to be created|`admin`|
|`storage.capacity`|Default disk size to be given to persistent volume|5Gi|
|`storage.accessModes`|Default access mode for volume|`['ReadWriteMany']`|
|`storage.hostPath`|Default path to be used in node|`/data/postgres`|
|`storage.mountPath`|Default path to be used in pod|`/var/lib/postgresql/data`|

## TODO
1. Fix chart installation
