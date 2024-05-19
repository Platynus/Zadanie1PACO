# Sprawozdanie z zadania1

### Wykonał Patryk Pawelec s97696

## Zadanie 1

### a. Informacja o dacie uruchomienia, imieniu i nazwisku autora oraz porcie TCP w logach:

Po uruchomieniu serwera, informacja o dacie uruchomienia, imieniu i nazwisku autora oraz porcie TCP, na którym serwer nasłuchuje, jest zapisywana do pliku server.log.
Kod realizujący to zadanie:
![image](https://github.com/Platynus/Zadanie1PACO/assets/56522713/5a84f108-5129-4488-b13b-a01c27127ead)
![image](https://github.com/Platynus/Zadanie1PACO/assets/56522713/d504e811-eb05-422d-a102-13a8e411f00b)


### b. Wyświetlenie strony z informacją o adresie IP klienta oraz dacie i godzinie w jego strefie czasowej:

Adres IP klienta jest pobierany za pomocą request.remote_addr.
Na podstawie tego adresu IP, serwer korzysta z API (https://ipinfo.io) do uzyskania informacji o strefie czasowej (dodatkowo dodałem możliwość zaczytywania lokalizacji).
Czas lokalny w strefie czasowej klienta jest obliczany i wyświetlany na stronie.
![image](https://github.com/Platynus/Zadanie1PACO/assets/56522713/9952697a-d0d4-4771-b5d6-4fdee3ed0d81)


## Zadanie 2

Został stworzony plik dockerFile i zostały wykonane następujące czynności:
- zbudowanie obrazu z punktu 1
- wykorzystanie warsty scratch
- optymalizacja pod katem fnkcjonowania cache w procesie budowaniea
- optymalizacja pod kątem warst
- dodanie healthcheck
- umieszczenie inforamacji o autorze
![image](https://github.com/Platynus/Zadanie1PACO/assets/56522713/34c6e773-10b1-49b4-be11-bcc132b27a6a)

## Zadanie 3

### a. Zbudowanie opracowanego obrazu kontenera:

docker build -t my-flask-app1 .

![image](https://github.com/Platynus/Zadanie1PACO/assets/56522713/96f421c6-19bb-40ab-8307-64fc25f70b4e)

### b. Uruchomienie kontenera na podstawie zbudowanego obrazu:

docker run -d -p 5000:5000 my-flask-app1

![image](https://github.com/Platynus/Zadanie1PACO/assets/56522713/1745c920-26da-4d7c-9f0a-dcfabb15f4f6)

![image](https://github.com/Platynus/Zadanie1PACO/assets/56522713/b8fc02ee-c976-48c1-824d-b61359d5b663)

### c. Sposób uzyskania informacji, które wygenerował serwer w trakcie uruchamiania kontenera:

docker logs --details   my-flask-app1

### d. Sprawdzenie, ile warstw posiada zbudowany obraz:

docker history my-flask-app1

![image](https://github.com/Platynus/Zadanie1PACO/assets/56522713/b90de812-56ae-4bd1-b2fd-730f04a6903a)

