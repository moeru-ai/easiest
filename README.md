# EasieST

![it works on my machine](https://img.shields.io/badge/it_works_on-my_machine-green)

Easy-to-use SillyTavern Starter, based on Docker Compose.

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

###### up / down

```bash
sudo docker compose up -d
# podman compose up -d # if you use podman

sudo docker compose down
# podman compose down # if you use podman
```

## FAQ

### Recommended Models (2024-04-06)

> If this section hasn't been updated in a long time, I recommend looking for a
> new model.

- 7B:
  [Lewdiculous/KukulStanta-7B-GGUF-IQ-Imatrix](https://huggingface.co/Lewdiculous/KukulStanta-7B-GGUF-IQ-Imatrix)
  - SillyTavern Presets:
    - [Lewdicu-Context-3.0.2-eros.json](https://huggingface.co/Lewdiculous/Eris_PrimeV4-Vision-32k-7B-GGUF-IQ-Imatrix/blob/main/sillytavern-presets-lewdicu-3.0.2-mistral-0.2/Lewdicu-Context-3.0.2-eros.json)
      => `./sillytavern/config/context`
    - [Lewdicu-Instruct-Alpaca-3.0.2-tentative.json](https://huggingface.co/Lewdiculous/Eris_PrimeV4-Vision-32k-7B-GGUF-IQ-Imatrix/blob/main/sillytavern-presets-lewdicu-3.0.2-mistral-0.2/Lewdicu-Instruct-Alpaca-3.0.2-tentative.json)
      => `./sillytavern/config/instruct`
    - [Lewdicu-Samplers-3.0.2.json](https://huggingface.co/Lewdiculous/Eris_PrimeV4-Vision-32k-7B-GGUF-IQ-Imatrix/blob/main/sillytavern-presets-lewdicu-3.0.2-mistral-0.2/Lewdicu-Samplers-3.0.2.json)
      => `./sillytavern/config/TextGen Settings`
- 70B:
  [mradermacher/Midnight-Miqu-70B-v1.5-i1-GGUF](https://huggingface.co/mradermacher/Midnight-Miqu-70B-v1.5-i1-GGUF)
  - SillyTavern Presets:
    - [prompting-tips](https://huggingface.co/sophosympatheia/Midnight-Miqu-70B-v1.5#prompting-tips)
      => `./sillytavern/config/context`
    - [instruct-formats](https://huggingface.co/sophosympatheia/Midnight-Miqu-70B-v1.5#instruct-formats)
      => `./sillytavern/config/instruct`
    - [sampler-tips](https://huggingface.co/sophosympatheia/Midnight-Miqu-70B-v1.5#sampler-tips)
      => `./sillytavern/config/TextGen Settings`

### Why llama.cpp?

`llama.cpp` provides the official docker image for Intel Arc Graphics.

I may change to `ollama` or `koboldcpp` later.

## License

[Unlicense](LICENSE)
