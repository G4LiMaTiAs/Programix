# GiftFlow 

## Informacje o projekcie
* uczelnia i wydział: Politechnika Białostocka Wydział Informatyki
* kierunek: Informatyka i Ekonometria
* przedmiot: Inżynieria Oprogramowania
* rok i semestr: 2 rok (semestr IV)
* grupa: 1
* temat:

Treść zadania projektowego 
Moduł Zarządzania Beneficjentami i Korespondencją
System GiftFlow służy do obsługi rocznego cyklu dystrybucji prezentów. Podstawowym podmiotem jest Beneficjent (posiadający unikalne ID, imię, nazwisko, wiek oraz dokładny adres z koordynatami GPS). Każdy Beneficjent może przesłać w danym roku dokładnie jeden List. List rejestrowany jest w systemie przez Elfa-Listonosza i zawiera listę życzeń oraz datę wpływu. Po rejestracji, system przesyła zapytanie do zewnętrznego systemu Grzecznościometr, który na podstawie danych behawioralnych zwraca Współczynnik Grzeczności (liczba 0-100).

Jeśli współczynnik jest mniejszy niż 50, List automatycznie otrzymuje status „Odrzucony”, co skutkuje utworzeniem zlecenia na Węgiel.

Jeśli współczynnik wynosi 50 lub więcej, List otrzymuje status „Zatwierdzony”, co inicjuje proces produkcji zabawek z listy życzeń.

Moduł Produkcji i Gospodarki Magazynowej
Zatwierdzony List generuje jedno lub więcej Zleceń Produkcyjnych. Każde Zlecenie przypisane jest do konkretnego Warsztatu (nazwa, lokalizacja). W Warsztacie pracuje Brygada Elfów – każdy Elf ma określoną specjalizację (np. stolarz, elektronik) i przypisany jest do jednego Warsztatu. Aby zrealizować Zlecenie, system musi zarezerwować i pobrać z Magazynu odpowiednie Surowce. Surowiec opisany jest przez nazwę, typ oraz aktualny stan magazynowy. Wynikiem pracy jest Prezent, który posiada unikalny kod QR, wagę, wymiary (szerokość, wysokość, głębokość) oraz status (np. „W produkcji”, „Gotowy”, „Spakowany”). Każdy Prezent przechodzi obowiązkową Kontrolę Jakości wykonywaną przez Elfa-Inspektora.

Moduł Logistyki, Załadunku i Transportu
Gotowe Prezenty grupowane są w Ładunki przypisane do konkretnego sektora geograficznego. Każdy Ładunek przypisany jest do Sani (unikalny numer rejestracyjny). Sanie mają określony techniczny limit Ładowności (kg) oraz Pojemności (m³). System posiada funkcję Balansowania, która rozmieszcza Prezenty w Saniach tak, aby środek masy był optymalny (blokada startu przy przeciążeniu).
Mikołaj (Główny Użytkownik) korzysta z modułu Nawigatora, który generuje Trasę jako listę Punktów Dostawy. Punkt Dostawy zawiera dane Beneficjenta i przewidywaną godzinę dotarcia (ETA). System w czasie rzeczywistym koryguje Trasę, pobierając dane z zewnętrznych modułów: GPS (aktualna pozycja) oraz Pogodynka (prędkość wiatru i opady).

Moduł Archiwizacji i Raportowania
Po dostarczeniu prezentu, Mikołaj oznacza go w systemie jako „Dostarczony”. 26 grudnia system automatycznie przenosi wszystkie dane z danego roku do Archiwum. Administrator systemu może wygenerować Raport Końcowy, który zawiera:

Zestawienie wydajności Warsztatów (liczba zrealizowanych zleceń).

Bilans zużycia Surowców.

Statystykę średniego czasu dostawy prezentu od momentu zatwierdzenia Listu.

[KLIKNIJ TUTAJ, ABY OTWORZYĆ PEŁNE SPRAWOZDANIE (PDF)](./sprawozdanie/Sprawozdanie_Finalne.pdf)

## Struktura plików (Dodatek A)
* [**/sprawozdanie**](./sprawozdanie) - wersja PDF oraz [**wersja edytowalna**](./sprawozdanie/edytowalne).
* [**/diagramy**](./diagramy) - źródła diagramów (UML).
* [**/interfejs**](./interfejs) - makiety UI.

   
