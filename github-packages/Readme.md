# Work with Container Images in GitHub packages

```sh
export GH_USERNAME="alexkasterin"
export GH_TOKEN=""
export GH_IMAGE_NAME="ping-alpine"
export GH_VER="v1.0.0"
```

```sh
echo $GH_TOKEN | docker login ghcr.io -u GH_USERNAME --password-stdin
```

```sh
docker build -t ${GH_IMAGE_NAME}:${GH_VER} .
```

```sh
docker tag ${GH_IMAGE_NAME}:${GH_VER} ghcr.io/${GH_USERNAME}/${GH_IMAGE_NAME}:${GH_VER}
```

```sh
docker push ghcr.io/${GH_USERNAME}/${GH_IMAGE_NAME}:${GH_VER}
```