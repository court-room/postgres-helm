postgres-helm
=============

## Setup
You can install this chart by cloning the repo and then installing as a local chart
```bash
helm install --set secrets.postgres_password=password postgres chart/postgres
```

## Configuration
You can provide the following configs for the Postgres Deployment

|Config                      |Description                                       |Default                   |
|:---                        |:---                                              |:---:                     |
|`config.POSTGRES_DB`        |Default database name to be created               |`postgres`                |
|`config.POSTGRES_USER`      |Default database user to be created               |`admin`                   |
|`secrets.postgres_password` |Default database password to be created           |                          |
|`config.storage.capacity`   |Default disk size to be given to persistent volume|5Gi                       |
|`config.storage.accessModes`|Default access mode for volume                    |`['ReadWriteMany']`       |
|`config.storage.hostPath`   |Default path to be used in node                   |`/data/postgres`          |
|`config.storage.mountPath`  |Default path to be used in pod                    |`/var/lib/postgresql/data`|

## TODO
1. Fix chart installation
