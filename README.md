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

### 起動

```bash
alias sail='[ -f sail ] && sh sail || sh vendor/bin/sail'
sail up
sail artisan migrate
```


