## Aggiungere autenticazione ad un progetto in corso

**0. comandi di setup**

- creazione file `.env`
- installa composer

```
composer i
```

- installa node

```
npm i
```

- crea chiave

```
php artisan key:generate
```

**1. modifichiamo questi file/cartelle:**

- (duplicazione) `routes/web.php` -> `routes/_web.php`
- (duplicazione) `resources/scss/app.scss` -> `resources/scss/_app.scss`
- (rinominare) `views` -> `_views`

**2. creiamo questi file:**

- `resources\views/welcome.blade.php`
- `resources\css/app.css`

**3.**

```
composer require laravel/breeze --dev
```

**4.**

```
php artisan breeze:install
```

**5.**

```
composer require pacificdev/laravel_9_preset
```

**6. cancelliamo la cartella: `resources\css`**

**7.**

```
php artisan preset:ui bootstrap --auth
```

**8.**

```
php artisan migrate:refresh
```

**9.**

```
npm i
```

**10.**

```
npm run dev
```

**11.**

```
php artisan serve
```
