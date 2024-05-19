#Sprawozdanie z zadania1

###Wykonał Patryk Pawelec s97696


##Zadanie 1

###a. Informacja o dacie uruchomienia, imieniu i nazwisku autora oraz porcie TCP w logach:

Po uruchomieniu serwera, informacja o dacie uruchomienia, imieniu i nazwisku autora oraz porcie TCP, na którym serwer nasłuchuje, jest zapisywana do pliku server.log.
Kod realizujący to zadanie:

###b. Wyświetlenie strony z informacją o adresie IP klienta oraz dacie i godzinie w jego strefie czasowej:

Adres IP klienta jest pobierany za pomocą request.remote_addr.
Na podstawie tego adresu IP, serwer korzysta z API (https://ipinfo.io) do uzyskania informacji o strefie czasowej (dodatkowo dodałem możliwość zaczytywania lokalizacji).
Czas lokalny w strefie czasowej klienta jest obliczany i wyświetlany na stronie.


##Zadanie 2

Został stworzony plik dockerFile i zostały wykonane następujące czynności:
- zbudowanie obrazu z punktu 1
- wykorzystanie warsty scratch
- optymalizacja pod katem fnkcjonowania cache w procesie budowaniea
- optymalizacja pod kątem warst
- dodanie healthcheck
- umieszczenie inforamacji o autorze

##Zadanie 3

###a. Zbudowanie opracowanego obrazu kontenera:

docker build -t my_web_server:1 .

###b. Uruchomienie kontenera na podstawie zbudowanego obrazu:

docker run -d -p 5000:5000 my_web_server:1

###c. Sposób uzyskania informacji, które wygenerował serwer w trakcie uruchamiania kontenera:

docker logs my_web_server:1

###d. Sprawdzenie, ile warstw posiada zbudowany obraz:

docker history my_web_server:1
