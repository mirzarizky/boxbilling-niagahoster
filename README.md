## Installation

Build up
```bash
docker-compose up -d --build
```

Install packages from composer
```bash
docker-compose exec composer install --working-dir=src --no-progress --no-suggest --prefer-dist --no-dev
```

Copy the config file
```bash
cp ./src/bb-config-sample.php ./src/bb-config.php
```

Prepare database
```bash
docker-compose exec php php ./bin/prepare.php
```

Delete the install folder from boxbilling
```bash
rm -rf src/install/*
```

You're good to go!

## DB Credentials
```
DB_NAME=boxbilling
DB_USER=root
DB_PASS=root
```