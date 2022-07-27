# Getting Start

- docker build

```bash
docker-compose build --no-cache
```

- bundle install

```bash
docker-compose run --rm api bundle config set path 'vendor/bundle'

docker-compose run --rm api bundle install
```

- Run docker

```bash
docker-compose up
```

- http://localhost:6000
