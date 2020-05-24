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

## 🐳 Docker installation and usage

### Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker-compose](https://docs.docker.com/compose/install/)

### Building and running

First, make sure you are inside this repository's directory:

```bash
cd <path/to/repo>
```

Then, start the container:

```bash
# start the container in the background of your terminal
docker-compose up --detach
```

At this point, the Jupyter Notebook will be running at `http://localhost:8888`.

### Installing new packages

There are a few ways you may install new packages to the container. It'll depend on your goal and needs.

#### Pip

If you need to do update or add packages via `pip`, execute the following command **inside your jupyter notebook**:

```bash
import sys

# install a pip package in the current Jupyter kernel
!{sys.executable} -m pip install <package>
```

> _**note**_: the `!` notation is used to run `pip` directly as a shell command from the notebook. Also, take a look [here](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/) to see why you should NOT use `!pip install <package>`.

#### Conda

If you need to do update or add packages via `conda`, execute the following command **inside your jupyter notebook**:

```bash
import sys

# install a conda package in the current Jupyter kernel
!conda install --yes --prefix {sys.prefix} <package>
```

> _**note**_: the `!` notation is used to run `conda` directly as a shell command from the notebook. Also, take a look [here](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/) to see why you should NOT use `!conda install --yes <package>`.

#### System

To add or update system packages, you will need `root` user permissions. To achieve this, use the following command:

```bash
# execute the container's shell
docker exec -it --user root tensorflow_notebook /bin/bash

# install a package to the system the container runs on
sudo apt install <package>
```

### Wrapping up

Once you're done, you may remove what was created by `up` with the following command:

```bash
# stop containers and removes containers, networks, volumes, and images created by `up`
docker-compose down
```

## 💻 Getting Started

TODO!

## 🤝 Contributing

If you are interested in helping contribute to the project, please take a look at our [Contributing Guide](CONTRIBUTING.md).

## 💡 Feedback

We'd love for you to take a short survey here (no more than five minutes): TODO!

## 📝 License

Copyright © 2020-present, [Cassandra Contributors](https://github.com/lcbm/cassandra/graphs/contributors).
This project is [ISC](LICENSE) licensed.
