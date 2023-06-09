# mi_docker_base
This repository is a development environment for Materials Informatics published by Assistant Professor <a href="https://researchmap.jp/mkumagai?lang=en">Masaya Kumagai</a> at Kyoto University.


## Prerequisites

- Git (windows user): https://gitforwindows.org/
- Docker Desktop: https://matsuand.github.io/docs.docker.jp.onthefly/desktop/
  - Docker
  - Docker-compose

## Installation

1. Clone this repository.
	```
	$ cd YOUR_WORKSPACE
	$ git clone https://github.com/kumagallium/mi_docker_base.git
	$ cd mi_docker_base
	```
2. Build the Docker image.
	```
	$ docker-compose build
	```
3. Start the Docker container.
	```
	$ docker-compose up
	```

4. Access the Jupyter Notebook at `http://localhost:8888` on your web browser.

## Usage of Pipenv

This repository uses Pipenv to manage packages. Below are some basic commands to use Pipenv.

- To install a package
	```
	$ docker-compose exec mi_docker_base pipenv uninstall [package name]
	```
- To install packages based on Pipfile.lock
	```
	$ docker-compose exec mi_docker_base pipenv install --ignore-pipfile
	```
- To install packages with development dependencies based on Pipfile.lock
	```
	$ docker-compose exec mi_docker_base pipenv install --dev
	```
- To remove the virtual environment based on Pipfile.lock
	```
	$ docker-compose exec mi_docker_base pipenv --rm
	```

For more detailed usage, refer to the official documentation.

## License

This repository is released under the MIT license. For more details, see the `LICENSE` file.








