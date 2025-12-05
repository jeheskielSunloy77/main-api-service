# pemad/main-api-service

## Install
composer require pemad-intl/main-api-service

## Publish config
php artisan vendor:publish --tag=mainapi-config

## .env

```env
MAIN_API_URL=https://example.test
MAIN_API_CODE=appcode
MAIN_API_SECRET=xxx
MAIN_API_KEY=vAWG...

## Usage
Resolve via container:
$api = app(\Pemad\MainApi\MainApiService::class);

example with options:
$response = $api->get('/api/user', ['limit' => 100]);
$response = $api->post('/api/sync', ['empl' => 69]);

example with headers:
$response = $api->get('/api/jabatan', [], [
    'accept_json' => true,
]);

## Artisan test
php artisan mainapi:test /api/health
