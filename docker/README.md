## Docker builds
Build YaakTech Darknet Image from [`docker`](https://github.com/yaak-ai/darknet/tree/docker) branch.

### Table

- [Prerequisites](https://github.com/yaak-ai/darknet/tree/docker/docker#prerequisites)
- Build Darknet
  - [CPU](https://github.com/yaak-ai/darknet/tree/docker/docker#darknet)
  - [GPU] (TODO)
- [Push Image to DockerHub](https://github.com/yaak-ai/darknet/tree/docker/docker#dockerhub)

#### Prerequisites
  1. Install docker for [Mac OS](https://www.docker.com/products/docker-desktop) or [Linux](https://docs.docker.com/engine/install/ubuntu/).
  2. `sudo usermod -aG docker $USER`
  3. Logout and Login again (for Linux)

#### Docker Compose

  Follow steps outlined [here](https://github.com/yaak-ai/darknet/blob/master/scripts/install_docker.sh)

#### Darknet
```
  docker-compose -f docker/ubuntu/docker-compose.yml build darknet-gpu
  docker-compose -f docker/ubuntu/docker-compose.yml build darknet-cpu
```

#### DockerHub
```
  docker-compose -f docker/ubuntu/docker-compose.yml push darknet-gpu
  docker-compose -f docker/ubuntu/docker-compose.yml push darknet-cpu
```
