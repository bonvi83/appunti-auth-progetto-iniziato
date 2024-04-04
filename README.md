## Aggiungere autenticazione ad un progetto in corso

**01. Comandi di setup**

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

**02. Modifichiamo questi file/cartelle:**

- (duplicazione) `routes/web.php` -> `routes/_web.php`
- (duplicazione) `resources/scss/app.scss` -> `resources/scss/_app.scss`
- (rinominare) `views` -> `_views`

**03. Creiamo questi file:**

- `resources\views/welcome.blade.php`
- `resources\css/app.css`

**04. Installiamo la dipendenza composer del pacchetto che si occupa dell'autenticazione**

```
composer require laravel/breeze --dev
```

**05. Installiamo alcuni file di supporto per breeze**

```
php artisan breeze:install
```

**06. Creiamo preset per togliere Tailwind e rimettere Bootstrap**

```
composer require pacificdev/laravel_9_preset
```

**07. Cancelliamo la cartella:** `resources\css` (perchè utilizzeremo l'scss)

**08. Per abilitare interfaccia per autenticazione e altro...**

```
php artisan preset:ui bootstrap --auth
```

**09. Refresh del database**

```
php artisan migrate:refresh
```

**10. Per sistemare alcune dipendenze del punto 08 e compilazione di NodeJS** (node)

```
npm i
```

```
npm run dev
```

**11. Avvio del server**

```
php artisan serve
```

### BUONA FORTUNA!
