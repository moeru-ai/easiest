# EasieST

Easy-to-use SillyTavern Starter via Docker Compose.

## Usage

###### clone

```bash
git clone https://github.com/moeru-ai/easiest.git
cd easiest
```

###### config

```bash
cp intel.docker-compose.yml docker-compose.yml # Intel oneAPI SYCL
# cp rocm.docker-compose.yml docker-compose.yml # AMD ROCm (TODO)
# cp cuda.docker-compose.yml docker-compose.yml # NVIDIA CUDA (TODO)
# cp vulkan.docker-compose.yml docker-compose.yml # Vulkan (TODO)

nano docker-compose.yml # edit config
```

###### run

```bash
sudo docker compose up -d
# podman compose up -d # if you use podman
```
