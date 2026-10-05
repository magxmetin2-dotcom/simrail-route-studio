# SimRail Route Studio

**Nieoficjalny kreator scenariuszy single player do [SimRail](https://store.steampowered.com/app/1422130/).** Zbuduj własny skład, wskaż stację początkową i docelową, a program sam dobierze semafory i przebiegi, po czym zapisze gotowy scenariusz do gry.

*Unofficial single-player scenario builder for SimRail. [English version below](#-english).*

**[⬇ Pobierz wersję 3.13.0 Beta](https://github.com/magxmetin2-dotcom/simrail-route-studio/releases/latest)** · Windows 10/11 (64-bit) · 44 MB · [Zgłoś błąd](https://github.com/magxmetin2-dotcom/simrail-route-studio/issues)

> [!NOTE]
> Nieoficjalny program Krzysztofa Maluhy. To nie jest narzędzie twórców SimRail i nie jest przez nich wspierane.

<!--
ZRZUTY EKRANU: zapisz pliki PNG w folderze docs/screenshots/ i usuń znaczniki komentarza wokół tych linii.
![Okno główne](docs/screenshots/okno-glowne.png)
![Własne trasy](docs/screenshots/wlasne-trasy.png)
-->

---

## 🇵🇱 Polski

### Co nowego w 3.13

- „Własne trasy” wybierają najkrótszą drogę w bazie (wcześniej: drogę z najmniejszą liczbą odcinków) i pokazują jej przybliżoną długość w km. Lista dostępnych celów liczy się szybciej.
- Tryb angielski: przetłumaczone komunikaty, raport diagnostyki i okno pierwszej konfiguracji. Tłumaczenie nie psuje już słów.
- Przy nieoczekiwanym błędzie program pokazuje krótki komunikat i zapisuje plik `crash.log` zamiast surowego okna błędu .NET.
- Folder roboczy `RouteStudioStaging` w folderze gry jest sprzątany po zapisie trasy.
- Baza tras i zgodna wersja gry są takie same jak w 3.12.0.

### Co potrafi

- **Własne trasy (próba)** – wybierz stację początkową, opcjonalne stacje „przez” i stację docelową na głównej mapie gry. Program sam dobierze najkrótszą drogę w bazie, semafory i przebiegi dyżurnego oraz pokaże przybliżoną długość trasy.
- **Kreator scenariusza** – własny skład z pojazdów z gry (lokomotywy, wagony, ładunki) na bazie oficjalnego scenariusza, z wyborem pory dnia, pogody, natężenia ruchu i opcjonalnym własnym rozkładem („Rozkład”).
- **Manewry** – misje manewrowe.
- **Bezpieczna praca** – projekty, zapisane składy, cofanie i ponawianie zmian oraz automatyczne odzyskiwanie pracy („Odzyskiwanie”).
- **Zarządzanie scenariuszami** – lista utworzonych scenariuszy, bezpieczne usuwanie z kopią zapasową i przywracanie kopii („Scenariusze”).
- **Paczki `.srspack`** – eksport i import scenariuszy, żeby dzielić się nimi z innymi graczami. Pliki są sprawdzane sumami SHA-256.
- **Narzędzia** – walidator scenariusza, kontrola DLC, mapa przejazdu, audyt przebiegów i diagnostyka logów gry.
- Interfejs po polsku i po angielsku.

### Wymagania

- Windows 10 (wersja 1809 lub nowsza) albo Windows 11, 64-bit.
- Własna instalacja SimRail. Scenariusz z pojazdem z DLC wymaga posiadania tego DLC.
- Około 220 MB miejsca na dysku. Środowisko .NET jest w zestawie, więc nic nie trzeba doinstalowywać ani pobierać. BepInEx nie jest potrzebny.

### Instalacja

1. Pobierz plik `SimRail-Route-Studio-3.13.0-Beta-Full-Offline-Setup.exe` ze strony [Releases](https://github.com/magxmetin2-dotcom/simrail-route-studio/releases/latest).
2. Zalecane: sprawdź sumę kontrolną pliku (patrz [Bezpieczeństwo i prywatność](#bezpieczeństwo-i-prywatność)).
3. Uruchom instalator. Nie potrzebuje uprawnień administratora. Domyślnie program trafia do `%LOCALAPPDATA%\Programs\SimRail Route Studio Beta`.

Instalator nie jest jeszcze podpisany cyfrowo, więc Windows może wyświetlić ostrzeżenie SmartScreen. Co wtedy zrobić, opisuje [FAQ](#najczęstsze-pytania).

Wersja beta instaluje się obok starszej wersji programu i jej nie usuwa. Jeśli masz już 3.12.0 Beta, instalator 3.13.0 ją zaktualizuje; ustawienia, projekty i scenariusze zostają.

### Jak utworzyć własną trasę

1. Uruchom **SimRail Route Studio Beta**. Jeśli program nie znajdzie gry, wskaż folder SimRail ręcznie.
2. W głównym oknie wybierz lokomotywę i wagony, a potem dodaj je przyciskiem **„＋ Dodaj”**. Pierwszy pojazd musi być lokomotywą albo zespołem trakcyjnym.
3. Kliknij **„Własne trasy (próba)”**. Wybierz stację początkową, opcjonalnie stacje „przez” i stację docelową.
4. Poczekaj, aż program dobierze drogę, i sprawdź listę stacji. Nie trzeba klikać „Wyznacz”.
5. Kliknij **„Zapisz do SimRail…”**, wpisz nazwę scenariusza (od 3 do 80 znaków) i potwierdź.
6. Jeśli SimRail był uruchomiony, uruchom go ponownie. W nowej grze single player wybierz scenariusz o tej nazwie.

Scenariusz trafia od razu do folderu gry (`SimRail_Data\StreamingAssets\Sceneries\1_KatowiceWarszawa\Scenarios`), więc nie trzeba niczego kopiować. Jeśli scenariusz o tej nazwie już istnieje, zapis zostanie odrzucony i nic nie zostanie nadpisane. Identyfikatory sygnałów znajdziesz w „Szczegółach technicznych”.

> [!IMPORTANT]
> „Przez” wyznacza przebieg drogi, a nie zaplanowany postój. Komunikat **„Accepted”** od dyżurnego oznacza tylko przyjęcie żądania przebiegu, a nie zezwolenie na jazdę. Zawsze obowiązują wskazania semaforów.

### Ograniczenia wersji beta

- Nie każda para stacji ma w bazie kompletne połączenie. Jeśli program nie znajduje drogi, nie znaczy to, że w grze jej nie ma.
- Program wybiera najkrótszą drogę w bazie. Długość trasy jest przybliżona (liczona z długości torów). Przebiegi w obie strony są szukane osobno.
- Nowa relacja i nowy skład wymagają przejazdu kontrolnego. Jazda kończy się przed wskazanym semaforem, bez gwarancji zatrzymania przy peronie.
- Nie ma rozkładu postojów pasażerskich ani połączenia z manewrami.
- Skład może mieć do ok. 300 m i 40 pozycji albo być jednym kompletnym zespołem trakcyjnym (EZT) bez doczepiania.
- Scenariusz zaczyna się latem o 9:00, misja trwa najwyżej 6 godzin, a czas przejazdu nie jest obliczany.
- Pogoda i postoje ustawione w kreatorze scenariuszy bazowych nie są przenoszone do własnych tras.

### Zgodność z wersją gry

Dołączona baza sieci pochodzi z odczytu z 8 września 2026 r. i pasuje do jednej konkretnej wersji gry. Program rozpoznaje tę wersję po sumie SHA-256 pliku `GameAssembly.dll`:

```
879CB08397DBA4660D04B2D96B17697152B465A725E7F33D5ABA1B54B64AD37C
```

Po aktualizacji SimRaila moduł „Własne trasy” może zgłosić niezgodność. To celowe zabezpieczenie przed tworzeniem scenariuszy, które w nowej wersji gry mogłyby nie działać. Nowa baza pojawi się w [Releases](https://github.com/magxmetin2-dotcom/simrail-route-studio/releases). Ta kontrola dotyczy tylko modułu „Własne trasy”.

### Bezpieczeństwo i prywatność

**Suma kontrolna instalatora 3.13.0 Beta (SHA-256):**

```
b864800da5a270c7bca547e5443f9bea77c6e35a1dbcf603e050af7711847dc5
```

Sprawdzisz ją w PowerShellu, w folderze z pobranym plikiem:

```powershell
Get-FileHash .\SimRail-Route-Studio-3.13.0-Beta-Full-Offline-Setup.exe -Algorithm SHA256
```

- **Bez internetu.** Program nie łączy się z siecią. Baza tras i .NET są w instalatorze. Przycisk „Uruchom” tylko otwiera grę przez Steam.
- **Bez ingerencji w kod gry.** Nie potrzeba uprawnień administratora ani BepInEx. Scenariusze korzystają wyłącznie z wbudowanych w SimRail skryptów Lua. Program nie wymusza stanów semaforów ani zwrotnic.
- **Oryginalne scenariusze zostają nietknięte.** Każdy nowy scenariusz powstaje jako osobny folder, a nieudany zapis jest automatycznie wycofywany. Przed usunięciem scenariusza program robi kopię zapasową.
- **Diagnostyka działa lokalnie.** Czyta logi gry na Twoim komputerze i maskuje m.in. ścieżkę profilu, SteamID i adresy e-mail. Przed udostępnieniem raportu i tak przejrzyj jego treść.
- **Paczki tylko z zaufanych źródeł.** Plik `.srspack` zawiera skrypt scenariusza wykonywany przez grę.

Gdzie program zapisuje pliki:

| Co | Gdzie |
|---|---|
| Program i baza tras | `%LOCALAPPDATA%\Programs\SimRail Route Studio Beta` |
| Kopie zapasowe scenariuszy | podfolder `Backups` w folderze programu |
| Ustawienia, projekty, składy, odzyskiwanie pracy, dziennik błędów `crash.log` | `%LOCALAPPDATA%\Krzysztof Maluha\SimRail Route Studio` |
| Utworzone scenariusze | nowe foldery `RTS_*` w `SimRail_Data\StreamingAssets\Sceneries\<mapa>\Scenarios` |

### Najczęstsze pytania

**Windows pokazuje komunikat „System Windows ochronił ten komputer”.**\
Instalator nie ma jeszcze podpisu cyfrowego, dlatego SmartScreen go nie rozpoznaje. Najpierw sprawdź sumę kontrolną (patrz wyżej). Jeśli się zgadza, kliknij „Więcej informacji”, a potem „Uruchom mimo to”.

**Nie widzę scenariusza w grze.**\
Uruchom SimRail ponownie, bo gra wczytuje listę scenariuszy przy starcie. Scenariusz znajdziesz w trybie single player.

**Program zgłasza niezgodną wersję gry.**\
SimRail dostał aktualizację, a dołączona baza tras pasuje do poprzedniej wersji. Poczekaj na nową bazę w Releases. Ta kontrola nie blokuje pozostałych funkcji programu.

**Program nie znajduje drogi między stacjami.**\
Wersja beta nie obsługuje każdej pary stacji. Spróbuj innej stacji „przez” albo krótszego składu, bo część punktów startowych ma za mało miejsca dla długiego pociągu.

**Czy to działa w trybie wieloosobowym?**\
Nie. Program tworzy wyłącznie scenariusze single player.

**Jak usunąć utworzone scenariusze?**\
Najprościej w programie: „Scenariusze” → wybierz scenariusz → usuń. Program zrobi kopię, którą można przywrócić na karcie „Kopie zapasowe”. Możesz też ręcznie usunąć folder `RTS_*` z folderu `Scenarios`, gdy gra jest wyłączona.

### Zgłaszanie błędów

Załóż zgłoszenie w zakładce [Issues](https://github.com/magxmetin2-dotcom/simrail-route-studio/issues). Napisz:

- jakiej wersji programu używasz,
- jaka była stacja początkowa, stacje „przez” i stacja docelowa,
- jaki był skład,
- co się stało, najlepiej ze zrzutem ekranu.

Pomoże też raport z „Diagnostyki”. Przejrzyj go przed wysłaniem.

Jeśli program pokazał komunikat o nieoczekiwanym błędzie, dołącz plik `crash.log` z folderu `%LOCALAPPDATA%\Krzysztof Maluha\SimRail Route Studio`. Ścieżki profilu i folderu gry, SteamID i adresy e-mail są w nim zamaskowane.

### Odinstalowanie

Ustawienia Windows → Aplikacje → **SimRail Route Studio Beta** → Odinstaluj.

Odinstalowanie nie usuwa scenariuszy z folderu gry, kopii zapasowych ani danych z `%LOCALAPPDATA%\Krzysztof Maluha\SimRail Route Studio`. Jeśli nie są Ci już potrzebne, usuń je ręcznie (lokalizacje są w tabeli wyżej).

---

## 🇬🇧 English

**Unofficial single-player scenario builder for [SimRail](https://store.steampowered.com/app/1422130/)** by Krzysztof Maluha. It is not made or supported by the SimRail developers. Build your own consist, pick a start and a destination, and the program selects the signals and dispatcher routes and saves a ready-to-play scenario into the game.

**[⬇ Download 3.13.0 Beta](https://github.com/magxmetin2-dotcom/simrail-route-studio/releases/latest)** · Windows 10/11 (64-bit) · 44 MB · [Report a bug](https://github.com/magxmetin2-dotcom/simrail-route-studio/issues)

### What's new in 3.13

- Custom routes now use the shortest path in the database (previously the path with the fewest segments) and show its approximate length in km. The list of reachable destinations is calculated faster.
- English mode: translated messages, diagnostics report and first-run window. Translation no longer garbles words.
- After an unexpected error the program shows a short message and writes `crash.log` instead of the raw .NET error window.
- The `RouteStudioStaging` work folder in the game folder is cleaned up after saving a route.
- The route database and the supported game build are the same as in 3.12.0.

### Features

- **Custom routes (preview)** – choose a start, optional *via* stations and a destination on the main game map. The shortest path in the database, the signals and the dispatcher routes are selected automatically, and the approximate length is shown.
- **Scenario builder** – your own consist from in-game vehicles (locomotives, wagons, cargo) based on an official scenario, with time of day, weather, traffic density and an optional custom timetable.
- **Shunting** – shunting missions.
- **Safe workflow** – projects, saved consists, undo/redo and automatic work recovery.
- **Scenario manager** – list of created scenarios, safe deletion with a backup, and restore.
- **`.srspack` packages** – export and import scenarios to share them, with SHA-256 checks.
- **Tools** – scenario validator, DLC check, journey map, route audit and game-log diagnostics.
- Polish and English interface.

### Requirements

- Windows 10 (1809 or later) or Windows 11, 64-bit.
- Your own SimRail installation. Scenarios with DLC vehicles require that DLC.
- About 220 MB of disk space. .NET is included, so nothing else needs to be installed or downloaded. No BepInEx required.

### Installation

1. Download `SimRail-Route-Studio-3.13.0-Beta-Full-Offline-Setup.exe` from [Releases](https://github.com/magxmetin2-dotcom/simrail-route-studio/releases/latest).
2. Recommended: verify the checksum (see [Security and privacy](#security-and-privacy)).
3. Run the installer. No administrator rights are needed. By default the program goes to `%LOCALAPPDATA%\Programs\SimRail Route Studio Beta`.

The installer is not digitally signed yet, so Windows SmartScreen may show a warning (see the [FAQ](#faq)). The beta installs next to the older version and does not remove it. If 3.12.0 Beta is installed, the 3.13.0 installer updates it; settings, projects and scenarios are kept.

### Creating a custom route

1. Launch **SimRail Route Studio Beta**. If your game is not detected, select the SimRail folder manually.
2. In the main window, pick a locomotive and wagons and add them with **＋ Add**. The first vehicle must be a locomotive or a multiple unit.
3. Click **Custom routes (preview)**. Choose a start, optional *via* stations and a destination.
4. Wait for the path to be calculated and review the station list. You do not need to press a separate button.
5. Click **Save to SimRail…**, enter a scenario name (3–80 characters) and confirm.
6. If SimRail was running, restart it. Select the scenario by its name in a new single-player game.

The scenario is saved straight into the game folder (`SimRail_Data\StreamingAssets\Sceneries\1_KatowiceWarszawa\Scenarios`). An existing name is rejected and nothing is overwritten. Signal IDs are shown under **Technical details**.

> [!IMPORTANT]
> *Via* is a routing point, not a scheduled passenger stop. **Accepted** from the dispatcher only means the route request was accepted, not that you may proceed. Always obey signals.

### Beta limitations

- Not every station pair is supported. If no path is found, the route may still exist in the game.
- The shortest path in the database is chosen. Its length is an estimate based on track lengths. Routes for each direction are searched separately.
- New routes and consists need an in-game trial run. The journey ends before the final signal, with no guaranteed platform stop.
- No passenger timetable or shunting integration.
- Consist limit: about 300 m and 40 entries, or one complete multiple unit without extra vehicles.
- Summer, 09:00 start, 6-hour mission limit; journey time is not calculated.
- Weather and stops set in the base scenario builder are not carried over to custom routes.

### Game version compatibility

The bundled network database was captured on 8 September 2026 and matches one specific game build, identified by the SHA-256 of `GameAssembly.dll` (`879CB08397DBA4660D04B2D96B17697152B465A725E7F33D5ABA1B54B64AD37C`). After a SimRail update the custom-route module may report an incompatible build. This is deliberate and prevents scenarios that might not work. Wait for an updated database in [Releases](https://github.com/magxmetin2-dotcom/simrail-route-studio/releases). The check applies only to the custom-route module.

### Security and privacy

**Installer checksum, 3.13.0 Beta (SHA-256):** `b864800da5a270c7bca547e5443f9bea77c6e35a1dbcf603e050af7711847dc5`

Verify it in PowerShell: `Get-FileHash .\SimRail-Route-Studio-3.13.0-Beta-Full-Offline-Setup.exe -Algorithm SHA256`

- **Offline.** The program makes no network connections. **Launch** only opens the game through Steam.
- **No changes to the game's code.** No administrator rights or BepInEx. Scenarios use only SimRail's built-in Lua scripting and never force signal or switch states.
- **Original scenarios stay untouched.** Each new scenario is a separate folder, failed saves are rolled back, and a backup is made before a scenario is deleted.
- **Local diagnostics.** Game logs are read on your computer and personal data such as your profile path, SteamID and e-mail addresses is masked. Review the report before sharing it.
- **Only import `.srspack` packages from people you trust.** A package contains a scenario script that the game runs.

Files are stored in `%LOCALAPPDATA%\Programs\SimRail Route Studio Beta` (program, database, `Backups`), `%LOCALAPPDATA%\Krzysztof Maluha\SimRail Route Studio` (settings, projects, consists, recovery, `crash.log`) and in the game folder (`RTS_*` scenario folders).

### FAQ

**Windows says "Windows protected your PC".** The installer is not signed yet, so SmartScreen does not recognise it. Verify the checksum first; if it matches, choose **More info** → **Run anyway**.

**The scenario does not appear in the game.** Restart SimRail; the game loads the scenario list at startup. Look for it in single player.

**The program reports an incompatible game version.** SimRail has been updated and the bundled database matches the previous build. Wait for a new database in Releases. This check does not block other features.

**No path is found.** Not every station pair is supported in the beta. Try another *via* station or a shorter consist.

**Does it work in multiplayer?** No. It creates single-player scenarios only.

**How do I remove created scenarios?** In the program: **Scenarios** → select → delete (a backup is kept and can be restored from the **Backups** tab). You can also delete the `RTS_*` folder from `Scenarios` while the game is closed.

### Reporting bugs

Open an [issue](https://github.com/magxmetin2-dotcom/simrail-route-studio/issues) with the program version, start/via/destination stations, your consist, what happened and ideally a screenshot. A report from **Diagnostics** helps too (review it first). If the program showed an unexpected-error message, attach `crash.log` from `%LOCALAPPDATA%\Krzysztof Maluha\SimRail Route Studio`; profile and game folder paths, SteamID and e-mail addresses are masked in it.

### Uninstalling

Windows Settings → Apps → **SimRail Route Studio Beta** → Uninstall. Scenarios in the game folder, backups and the data in `%LOCALAPPDATA%\Krzysztof Maluha\SimRail Route Studio` are kept; delete them manually if you no longer need them.

---

## Informacje prawne / Legal

SimRail i powiązane nazwy są znakami towarowymi ich właścicieli. Ten projekt nie jest powiązany z twórcami gry. Program jest udostępniany „tak jak jest”, bez żadnych gwarancji.

SimRail and related names are trademarks of their respective owners. This project is not affiliated with the game's developers. The program is provided "as is", without warranty of any kind.
