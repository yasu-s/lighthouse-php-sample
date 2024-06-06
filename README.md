# lighthouse-php-sample

## 環境

- Docker

## コマンド

### 初回

```bash
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php83-composer:latest \
    composer install --ignore-platform-reqs
```

```bash
cp .env.example .env
```

### 起動

```bash
./vendor/bin/sail up -d
./vendor/bin/sail artisan migrate
./vendor/bin/sail artisan db:seed --class=DatabaseSeeder
```

### エイリアス登録

```bash
alias sail='[ -f sail ] && sh sail || sh vendor/bin/sail'
```

## 挙動確認

- http://localhost/graphiql

## 参考URL

- https://laravel.com/docs/master/sail
- https://lighthouse-php.com/
