POMIARY RUCHU — wersja 1.0

URUCHOMIENIE NA KOMPUTERZE
Otwórz index.html w przeglądarce. Aplikacja nie wymaga bibliotek zewnętrznych.
Dla trwałego i przewidywalnego zapisu lepiej użyć lokalnego serwera HTTP:
  python -m http.server 8000
uruchomionego w tym folderze. Wejdź na http://localhost:8000.

IPHONE / INSTALACJA PWA
1. Rozpakuj ZIP. Udostępnij index.html, sw.js, manifest.webmanifest i icon.png
   w tym samym katalogu na statycznym hostingu HTTPS (np. GitHub Pages).
2. Otwórz publiczny adres strony w Safari na iPhonie.
3. Udostępnij -> Do ekranu początkowego -> Dodaj.
4. Uruchom aplikację, będąc online, aby zapisała pliki offline.
5. Przetestuj uruchomienie w trybie samolotowym przed wyjściem w teren.
Sam plik HTML z aplikacji Pliki na iOS nie gwarantuje działania JavaScript,
trwałego zapisu ani instalacji PWA. Hosting udostępnia jedynie pliki aplikacji;
projekty pozostają na urządzeniu, nie są przesyłane do hostingu.

POMIAR
Utwórz projekt, nadaj nazwę i sprawdź datę. Rozpocznij cykl o 06:00 lub 15:00
(możesz też włączyć wcześniej; licznik czeka na start). Godziny zmieniają się
zgodnie z czasem telefonu. Po 08:00 i 17:00 cykl kończy się automatycznie.
Wlot wybierasz w górnym rzędzie; każde dotknięcie komórki dodaje 1.
Piesi mają osobne przyciski L/P dla wszystkich wlotów.
W projekcie wybierz Korekta, aby dodać/odjąć zdarzenia w konkretnej godzinie.
Przerwanie lub spóźnienie jest oznaczane jako niepełny pomiar. Nie zamykaj
aplikacji w trakcie cyklu, jeśli chcesz zachować ciągłość pomiaru.

XLSX
Baza odtwarza układ A:O i wiersze 1:84 z czterowlotowego szablonu.
J = RO, K = T (zero), L = AP. M = piesi L, N = piesi P.
Piesi trafiają wyłącznie do bloku wlotu własnego (A-A, B-B, C-C, D-D).
B-B i D-D pozostają zerowe w kolumnach pojazdów. SUMA obejmuje pojazdy,
nie pieszych. Arkusze Status i Zdarzenia zawierają informacje uzupełniające.
Tabele prognoz nie są eksportowane. Zakres C4:N84 NIE jest przeznaczony do
wklejenia w całości (zawiera także nagłówki i sumy). Kopiuj dane C:N z samych
wierszy pomiarowych: 4–19, 25–40, 46–61, 67–82, do odpowiednich zakresów
w swoim oryginalnym arkuszu. Nie nadpisuj formuł w kolumnie O.

DANE
Zapis jest lokalny w localStorage. Kopia JSON pozwala przywrócić projekty.
Eksportuj kopię po każdym cyklu. Usunięcie danych Safari, tryb prywatny lub
zmiana adresu aplikacji mogą spowodować utratę dostępu do projektów.
Nie wykonuj pomiaru w dwóch kartach naraz. Blokada wygaszania ekranu zależy
od systemu. W razie potrzeby ustaw ręcznie dłuższą autoblokadę iPhone'a.
