## Kong and OpenID

Now spin up the kong-db service with the following command. The -d flag tells Docker Compose to run the process in the background:

```
$ docker-compose up -d kong-database
```

Verify the service is running (make sure State is "Up") :

```
$ docker-compose ps
```

Now we will run the migrations on the kong-db service. The following command will spin up a kong service, which will run the command kong migrations up. Due to the --rm flag, this service will be torn down after the command is run.

```
$  docker-compose run --rm kong kong migrations up
```

Finally, we can bring up Kong, and check if it's healthy (make sure State is "Up") :

```
$ docker-compose up -d kong

$ docker-compose ps
```
