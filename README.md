# Docker zadanie 2
Zadanie na labolatorium PwChO
# Uruchamianie
W celu uruchomienia LAMPa należy sklonować to repozytorium, a następnie uruchomić 1docker-compose1.

```
git clone https://github.com/bartoszziemba/dockercomposelab
docker-compose up
```
# Weryfikacja działania
Działanie apliacji można sprawdzić używając progamu `curl`.
```
curl localhost:6666
```
Wynikiem działania polecenia jest plik wynikowy html, czyli przetworzony plik php.

# Obrazy bazowe, wprowadzone zmiany
Proponowana implementacja usługi LAMP korzysta z oficjalnych obrazów `mariadb:10.1`, `httpd:2.4-alpine`, oraz `php:7.4-fpm-alpine`

Serwer apache wymagał dodatkowej konfiguracji w celu obsługi zewnętrznego serwera parsera php realizowanego w osobnym kontenerze. Konfiguracja została zrealizowana za pomocą pliku montowanego w odpowiednie miejsce. 

Serwer php wymagał zainstalowania rozszerzenia mysqli.

W przypadku bazy danych mariadb, żadna modyfikacja nie była wymagana.
