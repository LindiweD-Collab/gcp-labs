# GSP055 - Introduction to Docker

This directory contains the source code and Docker configuration for the "Introduction to Docker" lab on Google Cloud Skills Boosts.

## How to Build

```bash
docker build -t node-app:0.2 .
```
## How to Run
```bash
docker run -p 4000:80 --name my-app -d node-app:0.2
curl http://localhost:4000
```

## How to Push to Artifact Registry
```bash
docker tag node-app:0.2 us-east1-docker.pkg.dev/YOUR_PROJECT_ID/my-repository/node-app:0.2
docker push us-east1-docker.pkg.dev/YOUR_PROJECT_ID/my-repository/node-app:0.2
```
