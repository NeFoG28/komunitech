## Tutorial

1. Fork/clone repository ini

### Local

2. Duplikat file .env.example menjadi .env
```
copy .env.example .env
```
3. Jalankan composer install
```
composer install
```
4. Generate app key
```
php artisan key:generate
```
5. Jalankan migration beserta seedernya
```
php artisan migrate --seed
```
6. Jalankan perintah storage symbolic link
```
php artisan storage:link
```
7. Jalankan app
```
php artisan serve
```

### Docker

2. Duplikat file .env.example menjadi .env
```
cp .env.example .env
```
3. Jalankan composer install
```shell
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
```
4. Generate app key
```
sail artisan key:generate
```
5. Jalankan migration beserta seedernya
```
sail artisan migrate --seed
```
6. Jalankan perintah storage symbolic link
```
sail artisan storage:link
```
7. Jalankan app
```
sail up -d
```
