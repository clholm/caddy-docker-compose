# caddy-docker-compose
Use Docker Compose to deploy a website with Caddy

To use, set the `SRC` variable in this repo's `.env` file to the path to your website's source repo.

ex, in `.env`:
```
SRC={/path/to/your/repo}
```

Then, use `docker-compose` to build and run Caddy.

ex:
```
docker-compose -f docker-compose.yaml up
```
