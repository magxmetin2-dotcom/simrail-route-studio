# SIMRAIL ROUTE STUDIO 3.12.0 BETA — FULL OFFLINE

*Nieoficjalny program Krzysztofa Maluhy, nie narzędzie twórców SimRail.*
*Unofficial tool by Krzysztof Maluha.*

---

## 🇵🇱 POLSKI

### Instrukcja obsługi
1. Zainstaluj program i uruchom **„SimRail Route Studio Beta”**.
2. Wskaż swój folder SimRail, jeśli nie został wykryty automatycznie.
3. Wybierz lokomotywę i wagony w głównym oknie. Użyj **„Dodaj”**.
4. Otwórz **„Własne trasy (próba)”**. Wybierz początek, opcjonalnie „przez” i cel.
5. Poczekaj na automatyczne dobranie drogi. Sprawdź listę stacji.
6. Kliknij **„Zapisz do SimRail…”**, wpisz nazwę i potwierdź zapis.
7. W nowej grze single player wybierz tę nazwę. Jeśli SimRail był już uruchomiony, uruchom go ponownie, aby odświeżyć listę.

> **Ważne:** Scenariusz trafia do Twojego folderu gry: `SimRail_Data\StreamingAssets\Sceneries\1_KatowiceWarszawa\Scenarios`. Nie trzeba kopiować plików. Powtórzona nazwa jest odrzucana, nie nadpisywana. Semafory i przebiegi dobierane są automatycznie. Nie trzeba naciskać „Wyznacz”. Identyfikatory sygnałów dostępne są opcjonalnie w „Szczegółach technicznych”. „Przez” wskazuje przebieg drogi, NIE oznacza zaplanowanego postoju.

### Ograniczenia własnych dróg
* **Wydanie beta:** Nie każda para stacji ma kompletne połączenie w bazie. Program nie gwarantuje najkrótszej drogi. Przebiegi w obie strony są szukane osobno.
* **Przejazd kontrolny:** Nowa relacja i skład wymagają przejazdu kontrolnego. Koniec przed wskazanym semaforem, bez gwarancji peronu. Brak pasażerskiego rozkładu postojów i manewrów.
* **Limity:** Limit składu około 300 m, do 40 pozycji; jeden kompletny EZT bez doczepiania. Lato, 09:00, limit misji 6 h; czas przejazdu nie jest obliczany.
* Pogoda i postoje ustawione w kreatorze scenariuszy bazowych nie są przenoszone.
* *Accepted* = przyjęcie żądania, NIE zezwolenie na jazdę. Obowiązują sygnały.

### Zgodność
* Windows x64, Windows 10 1809 lub nowszy / Windows 11. Środowisko .NET dołączone.
* Wymagana własna instalacja SimRail i wymagane DLC. BepInEx nie jest potrzebny.
* **Dołączona baza:** odczyt 08.09.2026. Gra jest sprawdzana przez SHA256 `GameAssembly.dll`: `879CB08397DBA4660D04B2D96B17697152B465A725E7F33D5ABA1B54B64AD37C`. Jeśli gra jest inna, moduł wymaga nowej zgodnej bazy — nie wyłączaj tej kontroli.
* Instalator nie zawiera gry, prywatnych ustawień, projektów ani pluginów BepInEx. 
* To instalacja beta obok starej wersji. Odinstalowanie nie usuwa scenariuszy w grze ani projektów w profilu użytkownika. 
* Instalator nie jest podpisany cyfrowo; przed publikacją wydawca powinien go podpisać i zweryfikować zgodnie ze swoją polityką.

---

## 🇬🇧 ENGLISH

### Instructions
1. Install and launch **SimRail Route Studio Beta**.
2. Select your SimRail folder if automatic detection does not find it.
3. Add your locomotive and wagons in the main window.
4. Open **Custom routes (preview)**, choose the start, optional *via* station and destination. The path is calculated automatically.
5. Review the stations, choose **Save to SimRail**, enter a name and confirm.
6. Restart SimRail if it was running, then select that name in a new single-player game.

> **Note:** Via is a routing point, not a scheduled passenger stop. Not every station pair is supported. Signals and dispatcher routes are chosen separately for each direction. 

### Limitations
* New paths need an in-game trial. The shortest path is not guaranteed.
* No passenger timetable or shunting integration; stop before the final signal.
* Summer 09:00; 6-hour mission limit; journey time not calculated. 
* Consist limit approximately 300 m / 40 entries, or one complete multiple unit without wagons.
* *Accepted* does not mean permission to proceed. Obey signals.

### Compatibility
* Requires Windows x64, your own SimRail and DLC. .NET and network data included; no installation download or BepInEx required. 
* Game build must match the hash listed above; otherwise an updated database is required. 
* Beta installs next to the old app. Uninstall does not remove game scenarios or user projects. 
* Installer is not digitally signed.
