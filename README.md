<p align="center">
  <a target="_blank" rel="noopener noreferrer">
    <img src="docs/logo.png" alt="logo">
  </a>
</p>

<p align="center">
  <a href="https://opensource.org/licenses/ISC">
    <img src="https://img.shields.io/badge/License-ISC-yellow.svg" alt="License">
  </a>
  <a href="https://gitter.im/lcbm/community">
    <img src="https://badges.gitter.im/lcbm/community.svg" alt="Chat">
  </a>
</p>

# 👁️ Cassandra

> Cassandra was a priestess of Apollo in Greek mythology cursed to utter true prophecies, but never to be believed.

<insert>

## 🚀 Installation

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker-compose](https://docs.docker.com/compose/install/)

### Building and running

First, clone the project then make sure you are inside this repository's directory:

```bash
git clone https://github.com/lcbm/cassandra.git
cd cassandra
```

Now, start the container:

```bash
docker-compose up --detach # starts the container in the background of your terminal
```

### Installing new packages

If you wish to install additional packages to the container, do the following:

```bash
docker exec -it tensorflow_notebook /bin/bash # execute the container's bash
conda install <package> # or `pip install <package>`
```

If you need `root` permissions to do this, use the following command:

```bash
docker exec -it --user root tensorflow_notebook /bin/bash # execute the container's bash
sudo apt install <package>
```

### Wrapping up

Once you're done, you may remove what was created by `up` with the following command:

```bash
docker-compose down # stops containers and removes containers, networks, volumes, and images created by `up`
```

## 💻 Getting Started

<insert>

## 🤝 Contributing

If you are interested in helping contribute to the project, please take a look at our [Contributing Guide](https://github.com/lcbm/cassandra/blob/master/CONTRIBUTING.md).

## 💡 Feedback

We'd love for you to take a short survey here (no more than five minutes): <insert>

## 📝 License

Copyright © 2020-present, [Cassandra Contributors](https://github.com/lcbm/cassandra/graphs/contributors).
This project is [ISC](https://github.com/lcbm/cassandra/blob/master/LICENSE) licensed.
