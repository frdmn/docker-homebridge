# docker-homebridge

My docker-compose [homebridge](https://github.com/nfarina/homebridge) setup with support for Amazon Dash Buttons.

## Installation

1. Make sure you've installed all requirements
2. Clone this repository:

```shell
git clone https://github.com/frdmn/docker-homebridge
```

3. Create a copy of the sample `.env` file and adjust it at will:

```shell
cp .env.sample .env
```

4. Spin up the containers:

```shell
docker-compose up -d
```

## Configuration

You can make use of the following environment variables / configurations:

| Environment variable | Default value | Description
|----------------------|---------------|------------| 
| `PUID` | `0` | UID of executing user within container |
| `PGID` | `0` | GID of executing user within container |
| `PACKAGES` | `libpcap-dev` | Extra packages to install during creation |
| `TZ` | `Europe/Berlin` | Default timezone |

## Usage

### Services

#### Start/create services


```shell
$ docker-compose up -d
Creating homebridge_homebridge_1 ... done
```

#### Stop services

```shell
$ docker-compose stop
Stopping homebridge_homebridge_1 ... done
```

#### Upgrade services

```shell
$ docker-compose stop
$ docker-compose pull
$ docker-compose rm
$ docker-compose up -d
```

#### Check logs

```shell
$ docker-compose logs -f
```

```shell
$ docker-compose logs -f grafana
```

## Contributing

1. Fork it
2. Create your feature branch:

```shell
git checkout -b feature/my-new-feature
```

3. Commit your changes:

```shell
git commit -am 'Add some feature'
```

4. Push to the branch:

```shell
git push origin feature/my-new-feature
```

5. Submit a pull request

## Requirements / Dependencies

* Docker (incl. `docker-compose`)

## Version

1.0.0

## License

[MIT](LICENSE)
