# Craft 3 Docker

Easily create a CraftCMS development environment with Docker.

## Origin

Modified the original source to work easily on Mac docker environment.

- Added bridge networks
- Mounted local volume for MYSQL container so it won't erase after docker-compose down and docker-compose up
  Original source is from [bshelling](https://github.com/bshelling/craft-mac-n-cheez)

## Settings

Settings remain agnostic after bootstrap completion (i.e. file & folder permissions, credentials, structure). Settings are set by default or customized. For successful operation, it's assumed Docker, Docker Compose and Composer applications are installed. The images [bshelling/craftphpenv](https://cloud.docker.com/u/bshelling/repository/docker/bshelling/craftphpenv) and [mysql:5.7](https://hub.docker.com/_/mysql) are written to the docker-compose.yml.

### Requirements

[CraftCMS](https://www.craftcms.com)\
[Docker](https://www.docker.com)\
[Docker Compose](https://docs.docker.com/compose)\
[Composer](https://getcomposer.org/)

### Mac users

Before commanding the script below, install & turn on [Docker](https://docs.docker.com/docker-for-mac/install/)

### Commands

Check for Composer installation

```
$ composer -v
```

Check Docker & Docker Compose installation

```
$ docker -v && docker-compose -v
```

To run application

```
$ ./craftStarter.sh
```

To run it on Mac terminal

```
$ sh ./craftStarter.sh
```

### Default

Install CraftCMS at [http://localhost:8081/index.php?p=admin/install](http://localhost:8081/index.php?p=admin/install)

| Container Info     |                      |
| ------------------ | -------------------- |
| Docker Containers: | craft_web & craft_db |
| Port:              | 8081                 |

| Database Settings      |                    |
| ---------------------- | ------------------ |
| Host:                  | craft_db:3036      |
| Root Password:         | adminpwd           |
| Username:              | admin              |
| Password:              | adminpwd           |
| Default Database:      | craftdb            |
| Project Config Enabled | config/general.php |
