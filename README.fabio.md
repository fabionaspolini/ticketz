# Build my image

```bash
docker build -t fabionaspolini/ticketz-backend:latest --build-arg TICKETZ_REGISTRY_URL="http://localhost:3000" .
docker push fabionaspolini/ticketz-backend:latest

docker build -t fabionaspolini/ticketz-front:latest .
docker push fabionaspolini/ticketz-front:latest
```

# Execute my versions

```bash
docker compose -f docker-compose-fabio.yaml build && \
  docker compose -f docker-compose-fabio.yaml down -v && \
  docker compose -f docker-compose-fabio.yaml up -d
```

```bash
docker compose -f docker-compose-fabio-image.yaml up -d
docker compose -f docker-compose-fabio-image.yaml down -v
```