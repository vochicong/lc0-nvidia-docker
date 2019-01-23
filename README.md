Let's run [lc0](https://github.com/LeelaChessZero/lc0)
under [NVIDIA docker](https://github.com/NVIDIA/nvidia-docker).

# Run Lc0 self-play training games

To download and run the prebuilt Docker image

    docker run --runtime nvidia --rm -it vochicong/lc0-nvidia-docker

otherwise, clone this repository then build and run by

    docker-compose up --build lc0

# Run Lc0 with lichess-bot

- Download and put syzygy tablebases into `data/syzygy`
- Download and put networks (weights) into `data/networks`
- Edit lc0.config and lcbot-config.yml
- Put your `LICHESS_API_TOKEN` in file `.env` (NEVER git commit this file)

Run

    docker-compose up --build lcbot

# Requirements

- [nvidia-docker](https://github.com/NVIDIA/nvidia-docker)
- [docker-compose >= 1.23.2](https://github.com/docker/compose/releases)
