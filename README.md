# simrail-route-studio
Nieoficjalne narzędzie do tworzenia własnych tras i składów dla symulatora SimRail. / Unofficial custom route and consist builder for SimRail


# SIMRAIL ROUTE STUDIO 3.12.0 BETA — FULL OFFLINE[cite: 1]

*Nieoficjalny program Krzysztofa Maluhy, nie narzędzie twórców SimRail.*[cite: 1]
*Unofficial tool by Krzysztof Maluha.*[cite: 1]

---

## 🇵🇱 POLSKI[cite: 1]

### Instrukcja obsługi[cite: 1]
1. Zainstaluj program i uruchom „SimRail Route Studio Beta”.[cite: 1]
2. Wskaż swój folder SimRail, jeśli nie został wykryty automatycznie.[cite: 1]
3. Wybierz lokomotywę i wagony w głównym oknie.[cite: 1] Użyj „Dodaj”.[cite: 1]
4. Otwórz „Własne trasy (próba)”.[cite: 1] Wybierz początek, opcjonalnie „przez” i cel.[cite: 1]
5. Poczekaj na automatyczne dobranie drogi.[cite: 1] Sprawdź listę stacji.[cite: 1]
6. Kliknij „Zapisz do SimRail…”, wpisz nazwę i potwierdź zapis.[cite: 1]
7. W nowej grze single player wybierz tę nazwę.[cite: 1] Jeśli SimRail był już uruchomiony, uruchom go ponownie, aby odświeżyć listę.[cite: 1]

**Ważne informacje:**
* Scenariusz trafia do Twojego folderu gry: `SimRail_Data\StreamingAssets\Sceneries\1_KatowiceWarszawa\Scenarios`.[cite: 1]
* Nie trzeba kopiować plików.[cite: 1] Powtórzona nazwa jest odrzucana, nie nadpisywana.[cite: 1]
* Semafory i przebiegi dobierane są automatycznie.[cite: 1] Nie trzeba naciskać „Wyznacz”.[cite: 1]
* Identyfikatory sygnałów dostępne są opcjonalnie w „Szczegółach technicznych”.[cite: 1]
* „Przez” wskazuje przebieg drogi, NIE oznacza zaplanowanego postoju.[cite: 1]

### OGRANICZENIA WŁASNYCH DRÓG[cite: 1]
* **Wydanie beta:** Nie każda para stacji ma kompletne połączenie w bazie.[cite: 1] Program nie gwarantuje najkrótszej drogi.[cite: 1] Przebiegi w obie strony są szukane osobno.[cite: 1]
* **Przejazd kontrolny:** Nowa relacja i skład wymagają przejazdu kontrolnego.[cite: 1] Koniec przed wskazanym semaforem, bez gwarancji peronu.[cite: 1] Brak pasażerskiego rozkładu postojów i manewrów.[cite: 1]
* **Limity:** Limit składu około 300 m, do 40 pozycji; jeden kompletny EZT bez doczepiania.[cite: 1] Lato, 09:00, limit misji 6 h; czas przejazdu nie jest obliczany.[cite: 1]
* Pogoda i postoje ustawione w kreatorze scenariuszy bazowych nie są przenoszone.[cite: 1]
* *Accepted* = przyjęcie żądania, NIE zezwolenie na jazdę.[cite: 1] Obowiązują sygnały.[cite: 1]

### ZGODNOŚĆ[cite: 1]
* Windows x64, Windows 10 1809 lub nowszy / Windows 11.[cite: 1] Środowisko .NET dołączone.[cite: 1]
* Wymagana własna instalacja SimRail i wymagane DLC.[cite: 1] BepInEx nie jest potrzebny.[cite: 1]
* **Dołączona baza:** odczyt 08.09.2026.[cite: 1] Gra jest sprawdzana przez SHA256 `GameAssembly.dll`: `879CB08397DBA4660D04B2D96B17697152B465A725E7F33D5ABA1B54B64AD37C`.[cite: 1] Jeśli gra jest inna, moduł wymaga nowej zgodnej bazy — nie wyłączaj tej kontroli.[cite: 1]
* Instalator nie zawiera gry, prywatnych ustawień, projektów ani pluginów BepInEx.[cite: 1]
* To instalacja beta obok starej wersji.[cite: 1] Odinstalowanie nie usuwa scenariuszy w grze ani projektów w profilu użytkownika.[cite: 1]
* Instalator nie jest podpisany cyfrowo; przed publikacją wydawca powinien go podpisać i zweryfikować zgodnie ze swoją polityką.[cite: 1]

---

## 🇬🇧 ENGLISH[cite: 1]

### Instructions[cite: 1]
1. Install and launch **SimRail Route Studio Beta**.[cite: 1]
2. Select your SimRail folder if automatic detection does not find it.[cite: 1]
3. Add your locomotive and wagons in the main window.[cite: 1]
4. Open **Custom routes (preview)**, choose the start, optional *via* station and destination.[cite: 1] The path is calculated automatically.[cite: 1]
5. Review the stations, choose **Save to SimRail**, enter a name and confirm.[cite: 1]
6. Restart SimRail if it was running, then select that name in a new single-player game.[cite: 1]

**Note:**
* Via is a routing point, not a scheduled passenger stop.[cite: 1]
* Not every station pair is supported.[cite: 1]
* Signals and dispatcher routes are chosen separately for each direction.[cite: 1]

### Limitations[cite: 1]
* New paths need an in-game trial.[cite: 1] The shortest path is not guaranteed.[cite: 1]
* No passenger timetable or shunting integration; stop before the final signal.[cite: 1]
* Summer 09:00; 6-hour mission limit; journey time not calculated.[cite: 1]
* Consist limit approximately 300 m / 40 entries, or one complete multiple unit without wagons.[cite: 1]
* *Accepted* does not mean permission to proceed.[cite: 1] Obey signals.[cite: 1]

### Compatibility[cite: 1]
* Requires Windows x64, your own SimRail and DLC.[cite: 1] .NET and network data included; no installation download or BepInEx required.[cite: 1]
* Game build must match the hash listed above; otherwise an updated database is required.[cite: 1]
* Beta installs next to the old app.[cite: 1] Uninstall does not remove game scenarios or user projects.[cite: 1]
* Installer is not digitally signed.[cite: 1]
