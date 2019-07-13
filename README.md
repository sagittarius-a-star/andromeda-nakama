# andromeda-nakama

Backend server for Andromeda project. Using Nakama to quickly get started.

Nakama server Docker instructions can be found here: https://heroiclabs.com/docs/install-docker-quickstart/

## Starting the Stack

```shell
# bring the stack online in detached mode
docker-compose up -d

# verify the stack is running
docker ps
```

There should be two containers running, `andromeda-nakama-cdb` and `andromeda-nakama`.

## Developer Console

Once the stack is online, you can login to the developer console by opening a browser to `http://localhost:7351` or `http://127.0.0.1:7351`.

Thee default username and password:

```shell
# username
admin

# password
password
```

These default settings can be changed via the Nakama configuration file. Check this out for details: https://github.com/heroiclabs/nakama-docs/blob/master/docs/install-configuration.md.

## LUA scripts

When the Docker instance starts, it will create a `./nakama/data/modules/` folder in the repo directory and mount it in the Docker instance.

LUA scripts can be added to the `./nakama/data/modules/` to be made available to the server.

## Stopping the Stack

```shell
# from the repo directory
docker-compose down
```
