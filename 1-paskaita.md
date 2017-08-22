# Laravel: 1 paskaita

## Apie ką kalbėjome ir ką nuveikėme

1. [PHP FIG](http://php-fig.org): [PSR1](http://www.php-fig.org/psr/psr-1/) (Basic Coding Standard), [PSR2](http://www.php-fig.org/psr/psr-2/) (Coding Style Guide)

2. [Composer](https://getcomposer.org): PHP paketų valdymo įrankis, diegimas savo kompiuteryje

3. [Packagist](https://packagist.org): pagrindinė Composer paketų repozitorija (saugykla)

4. CLI (komandinės eilutės) pagrindai:

`cd DIR_PATH` - pereiti į nurodytą direktoriją

`dir` - išsivesti direktorijos, kurioje esame, turinį

`mkdir DIR_TITLE` - sukurti naują direktoriją

`echo. > FILE_PATH` - sukurti naują tuščią tekstinį failą

5. Composer komandos, `composer.json` failas

`composer install` - įrašyti composer.json faile nurodytus paketus
`composer require autorius/paketas` - pridėti naują paketą į jau egzistuojantį projektą

```json
{
    "require": {
        "autorius/paketas": "versija"
    }
}
```

6. [Laravel](https://laravel.com): įsirašymas naudojantis Composer dviem būdais:

```
composer create-project --prefer-dist laravel/laravel blog`
```

arba

```
composer global require laravel/installer
laravel new blog
```

P.s. abiem atvejais vietoje `blog` gali būti bet koks pavadinimas jūsų direktorijai, kurioje atsiras naujas projektas.

7. Xampp konfigūravimas įvedant host'ą `laravel.dev` arba `php artisan serve`

Naujas Apache vHost įrašas (C:\xampp\apache\conf\extra\httpd-vhosts.conf):

```
<VirtualHost laravel.dev:80>
  DocumentRoot "C:\xampp\htdocs\laravel\public"
  ServerAdmin laravel.dev
  <Directory "C:\xampp\htdocs\laravel">
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
  </Directory>
</VirtualHost>
```

Hosts failo papildymas (C:\Windows\System32\drivers\etc\hosts):

```
127.0.0.1	laravel.dev
```

8. Laravel default welcome puslapio nuorodos: [dokumentacija](https://laravel.com/docs/5.4), [Laracasts](https://laracasts.com/), [Laravel News](https://laravel-news.com/), [Forge](https://forge.laravel.com)

9. Laravel failų sistemos apžvalga

11. Public katalogas, kuris yra pagrindinis web serveriui ir atėjusiam vartotojui: `public`

10. Views katalogas, welcome view ir pirmieji pakeitimai: `resources/views`, `resources/views/welcome.blade.php`

11. Routes katalogas ir pirmieji pakeitimai: `routes/web.php`

12. Nauji Routes ir Views: /about (tekstas), /contact-us (kuriam paprastą kontaktinę formą su HTML)

13. MVC (model-view-controller) patterno paaiškinimas

## Video

[Paskaita nr. 1 - YouTube](https://www.youtube.com/watch?v=AHWGjm_3Dcs)

## Užduotys

1. Patobulinam savo Atom editorių įsidiegdami šiuos pluginus:

* https://atom.io/packages/php-cs-fixer (atsiras komanda, kuri suformatuoja kodą pagal PSR-2)

* https://atom.io/packages/linter-php (jeigu kode bus sintaksės klaidų ar pan., editorius raudonuos blogą vietą ir lieps taisyti)

2. Peržiūrim 8 punkte išvardintas nuorodas. Pavaikštom po dokumentaciją, paskaitom naujienas, užsiprenumeruojam naujienlaiškį, patikrinam Laravel News FB puslapį, prisijunkim prie mano minėto pulso. Puiku būtų pasidairyti ir po nemokamas Laracasts video pamokas žinioms užtvirtinti. Kuo daugiau skirtingų šaltinių mokymuisi naudosit, tuo daugiau naudos gausit. Jeigu reikia pagalbos - aš visada jums pasiekiamas :)

3. Užsiregistruojam https://www.codewars.com/, susikuriam savo profilį. Kadangi esate naujokai ir programavimo praktika yra labai reikalinga, kai jau žinote daug teorijos, pamėginkim laisvu laiku paspręsti įvairias užduotis JS ar PHP kalbomis. Kol kas laisvai, vėliau galėsim apie tai padiskutuoti daugiau, pasirinkti konkrečias užduotis visiems.
