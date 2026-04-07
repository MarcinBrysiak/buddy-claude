# Buddy-Claude v2 — Design Spec

**Data:** 2026-04-07
**Autor:** Marcin + Claude
**Status:** Draft

## Kontekst

Buddy-Claude v1 to plugin szkoleniowy dla zespolu marketingu InPost (20 osob).
Po przejsciu calego flow v1, zebrano feedback ktory wskazuje na braki w:
- personalizacji (imie uczestnika)
- wprowadzeniu do interfejsu Cowork (tryby, elementy nawigacji)
- slowniku pojec na starcie
- wyjasnieniu superpowers
- flow Projects (tworzenie projektu step by step)
- interaktywnym tworzeniu CLAUDE.md pod role uczestnika

## Decyzje projektowe

| Temat | Decyzja |
|-------|---------|
| Personalizacja | Pytanie o imie na starcie, uzywane przez cala sesje |
| Instalacja pluginu | Na zywo pod okiem Marcina |
| Tryby Chat/Cowork/Code | Focus na Cowork, reszta "poznacie w przyszlosci" |
| Projects | Kazdy uczestnik wybiera swoj obszar i robi kompletny projekt |
| Skille/pluginy | Uzywaja zanim wiedza czym sa, modul wyjasnia retrospektywnie |
| Slownik | Osobny modul na poczatku kursu |
| CLAUDE.md | Prosty w module + dopracowany w finalnym projekcie |
| Podejscie | Ewolucja obecnej struktury — 14 krokow (z 10) |

## Nowa sciezka szkoleniowa — 14 krokow

| Krok | Typ | Temat | Plik zrodlowy | Status |
|------|-----|-------|---------------|--------|
| 0 | Powitanie | Imie + instalacja + orientacja | SKILL.md (inline) | Nowy |
| 1 | Modul | Slownik podstawowy | modules/01-glossary.md | Nowy |
| 2 | Modul | Ekosystem Claude | modules/02-ecosystem.md | Update |
| 3 | Cwiczenie | Pierwsza rozmowa | exercises/ex01-first-chat.md | Minor update |
| 4 | Modul | Poruszanie sie po Cowork | modules/03-navigation.md | Update |
| 5 | Cwiczenie | Techniki promptowania | exercises/ex02-prompting.md | Minor update |
| 6 | Modul | Sztuka promptowania | modules/04-prompting.md | Update |
| 7 | Cwiczenie | Praca z kontekstem | exercises/ex03-context.md | Minor update |
| 8 | Modul | Skille i pluginy | modules/05-skills-plugins.md | Update |
| 9 | Cwiczenie | Korzystanie ze skilli | exercises/ex04-skills-usage.md | Minor update |
| 10 | Modul | Pliki konfiguracyjne + interaktywny CLAUDE.md | modules/06-md-files.md | Update |
| 11 | Cwiczenie | Stworz swoj pierwszy CLAUDE.md | exercises/ex05-claude-md.md | Nowy |
| 12 | Modul | Projects — Twoja przestrzen pracy | modules/07-projects.md | Nowy |
| 13 | Cwiczenie | Wlasny projekt od zera | exercises/ex06-own-project.md | Nowy |

**Usuwany plik:** exercises/ex05-real-task.md (zastapiony przez ex05-claude-md.md + ex06-own-project.md)

## Szczegoly nowych i zmienionych elementow

### Krok 0: Powitanie (SKILL.md inline)

Flow:
1. Pytanie o imie: "Jak masz na imie?"
2. Spersonalizowane powitanie: "Czesc [imie]!"
3. Kontekst instalacyjny: "Skoro masz buddy-claude — swietnie! Pozniej wyjasnime czym jest plugin."
4. Przeglad kursu uproszczony do 3 blokow (nie 14 krokow):
   - Podstawy i ekosystem
   - Prompting i praca z materialami
   - Wlasny projekt
5. Buddy-Claude uzywa imienia przez cala sesje — naturalnie, nie w kazdym zdaniu.

### Krok 1: Modul Slownik (modules/01-glossary.md) — NOWY

Podejscie: rozmowa, nie suchy slownik. 4 grupy pojec, po kazdej "Czy to jasne?":

**Grupa 1 — Podstawowe:**
- Prompt (brief do grafika)
- Kontekst (informacje dla Claude)
- Model (mozg Claude — Haiku/Sonnet/Opus jak junior/mid/senior)
- Token (jednostka tekstu, jak znaki w SMS)
- Markdown (formatowanie — gwiazdki, hasztagi)

**Grupa 2 — Claude Code:**
- Claude Code (narzedzie w ktorym jestes)
- Desktop App (aplikacja — Chat/Cowork/Code, my uzywamy Cowork, reszta w przyszlosci)
- Slash command (komendy z `/`)
- Permission (Claude pyta o pozwolenie)

**Grupa 3 — Rozszerzenia:**
- Plugin (rozszerzenie przegladarki)
- Skill (szablon w Canva)
- MCP (podlaczanie narzedzi — Gmail, kalendarz)
- Hook (automatyczna akcja)
- CLAUDE.md (instrukcje, brand book)

**Grupa 4 — Zaawansowane (wzmianka, nie deep dive):**
- API, agent, sub-agent, plan mode, worktree, tool use, Enterprise plan
- "Te pojecia poznasz w przyszlosci z Marcinem."

Zakonczenie: "W kazdej chwili wpisz `/explain <pojecie>` i przypomne Ci."

### Krok 2: Modul Ekosystem (modules/02-ecosystem.md) — UPDATE

Zmiany wzgledem obecnego 01-ecosystem.md:
- Usuniecie duplikacji ze slownikiem (pojecia juz wyjasione w kroku 1)
- Nowa sekcja: Tryby Claude — Chat/Cowork/Code
  - Chat: prosty czat, w przyszlosci
  - Cowork: desktop app z plikami, "tu jestesmy"
  - Code: terminal dla devow, "domena Marcina"
- Nowa sekcja: Gdzie Claude pracuje — dysk C, home, user
  - Analogia: biurko Claude
  - Fundamentalne dla zrozumienia Projects w kroku 12

### Krok 3: Cwiczenie Pierwsza rozmowa — MINOR UPDATE

Bez zmian w strukturze. Dodanie personalizacji imieniem w feedbacku.

### Krok 4: Modul Nawigacja (modules/03-navigation.md) — UPDATE

Zmiany wzgledem obecnego 02-navigation.md:
- Zachowane: interfejs, rozmowy, slash commands
- Nowa sekcja: Elementy nawigacji Cowork (2-3 zdania + analogia per element):
  - Search — przeszukiwanie rozmow
  - Projects — przestrzenie pracy ("szczegoly w module 7")
  - Ideas — szybkie notatki
  - Customize — ustawienia, pluginy
  - Scheduled — zaplanowane zadania ("zaawansowane, w przyszlosci")
  - Dispatch — wysylanie zadan ("zaawansowane, w przyszlosci")
- Rozbudowana sekcja o kontekscie rozmowy

### Krok 5: Cwiczenie Prompting — MINOR UPDATE

Personalizacja imieniem w feedbacku.

### Krok 6: Modul Prompting (modules/04-prompting.md) — UPDATE

Minimalne zmiany — sprawdzona tresc. RKKF, iteracja, dobre vs zle prompty.

### Krok 7: Cwiczenie Kontekst — MINOR UPDATE

Personalizacja imieniem w feedbacku.

### Krok 8: Modul Skille i pluginy (modules/05-skills-plugins.md) — UPDATE

Zmiany wzgledem obecnego 04-skills-plugins.md:
- Moment "aha" na starcie: "[Imie], pamietasz jak instalowales buddy-claude? To wlasnie byl plugin ze skillem."
- Nowa sekcja: Superpowers
  - Oficjalny plugin od Anthropic
  - Dodaje "supermoce" — planowanie, brainstorming, debugging
  - Dziala automatycznie w tle
  - Analogia: GPS w samochodzie
  - "Nie musisz sie tym zajmowac"
- Nowa sekcja: Customize -> Personal plugins
  - Skad brac pluginy (marketplace)
  - Retrospektywne wyjasnienie instalacji buddy-claude
- Update sekcji "co nadchodzi" — AI INPOST TOWER

### Krok 9: Cwiczenie Skille — MINOR UPDATE

Personalizacja imieniem w feedbacku.

### Krok 10: Modul CLAUDE.md (modules/06-md-files.md) — UPDATE

Zmiany wzgledem obecnego 05-md-files.md:
- Zachowane: problem pamieci, CLAUDE.md jako brand book, markdown, analogia samochodu
- Nowa sekcja: Interaktywne wyjasnienie CLAUDE.md
  - Buddy-Claude pyta: "Czym sie zajmujesz? Np. analityka, Adwords, content?"
  - Po odpowiedzi: wzorcowa struktura CLAUDE.md dopasowana do roli
  - Przyklad dla content managera:
    ```
    # Rola
    Jestem content managerem InPost. Tworze tresci na social media.
    # Zasady
    - Pisz po polsku
    - Tone of voice: przyjazny, bezposredni
    # Format
    - Posty max 280 znakow (Twitter) / 2200 (Instagram)
    ```
- Wyjasnienie gdzie zyje CLAUDE.md — w folderze projektu, czytany automatycznie

### Krok 11: Cwiczenie Stworz CLAUDE.md (exercises/ex05-claude-md.md) — NOWY

Struktura:
1. Buddy-Claude zadaje 4 pytania: rola, typowe zadania, ton komunikacji, zasady/ograniczenia
2. Uczestnik SAM pisze swoj CLAUDE.md (Buddy-Claude nie pisze za niego)
3. Buddy-Claude daje feedback i sugeruje ulepszenia
4. Test: nowa rozmowa, sprawdzenie czy Claude zachowuje sie zgodnie z CLAUDE.md

Kluczowy przekaz: "To pierwsza konfiguracja. W finalnym projekcie dopracujesz ja na powaznie."

### Krok 12: Modul Projects (modules/07-projects.md) — NOWY

**Sekcja 1: Co to jest Project?**
- Analogia: segregator na biurku
- Kazdy project ma folder, pliki, CLAUDE.md

**Sekcja 2: Tworzenie projektu — krok po kroku**
- Projects -> Create new project
- 3 opcje z wyjasnieniem:
  - Start from scratch — pusty segregator
  - Import a project — repo z GitHub
  - Use an existing folder — istniejacy folder z plikami
- Na szkoleniu: Start from scratch

**Sekcja 3: Anatomia projektu**
- Folder na dysku C (nawiazanie do modulu 2)
- CLAUDE.md w projekcie (nawiazanie do modulu 6)
- Przelaczanie miedzy projektami

**Sekcja 4: Propozycje zastosowan**
- Analityk: analiza danych, raporty tygodniowe
- Adwords: optymalizacja kampanii, analiza wynikow
- Content: brand voice, generowanie postow
- Ogolny: prezentacje, raporty, Excel

### Krok 13: Cwiczenie finalne — Wlasny projekt (exercises/ex06-own-project.md) — NOWY

**Struktura (20-30 min):**

1. **Wybor obszaru** — Buddy-Claude pyta o codzienna prace, propozycje:
   - Analityka (raporty, dane, Excel)
   - Kampanie (Adwords, performance, budzety)
   - Content (social media, copywriting, brand voice)
   - Prezentacje i raporty korporacyjne
   - Cos innego

2. **Tworzenie projektu step by step:**
   - Krok 1: "Kliknij Projects w bocznym menu. Widzisz?"
   - Krok 2: "Kliknij Create new project. Pojawily sie 3 opcje?"
   - Krok 3: "Wybierz Start from scratch. Wpisz nazwe, np. 'Analityka-Mobile'."
   - Krok 4: "Widzisz pusty projekt. To Twoja przestrzen pracy."
   - Krok 5: Tworzenie CLAUDE.md (pytania o role, zadania, ton, zasady)
   - Krok 6: "CLAUDE.md gotowy! Napisz pierwsze zadanie."
   - Kazdy krok: instrukcja -> czekanie na potwierdzenie -> feedback -> nastepny
   - Buddy-Claude NIE przeskakuje nawet jesli uczestnik mowi "zrobilem 1-3"

3. **CLAUDE.md na powaznie** — dopracowany pod realny projekt (bazujac na doswiadczeniu z kroku 11)

4. **Pierwsze realne zadanie** — jedno zadanie w projekcie

5. **Refleksja** — co poszlo dobrze, co by zmienil, jakie kolejne zadania

Kluczowy przekaz: "Wychodzisz ze szkolenia z dzialajacym projektem. Od jutra mozesz go uzywac w pracy."

## Zakonczenie kursu

Update obecnego zakonczenia:
- Gratulacje z imieniem
- Lista umiejetnosci (rozszerzona o Projects i CLAUDE.md)
- Przydatne komendy: /explain, /hint, /tutorial, /exercise
- Odeslanie do Marcina (AI Champion) dla zaawansowanych tematow

## Zmiany w CLAUDE.md pluginu

- Aktualizacja opisu o nowe moduly i cwiczenia
- Dodanie instrukcji personalizacji (imie)
- Update glownej komendy /buddy-claude na 14 krokow

## Zmiany w /explain skill

- Weryfikacja ze slownik pokrywa wszystkie pojecia z 4 grup z kroku 1
- Dodanie brakujacych pojec jesli sa

## Szacowany czas szkolenia

~4 godziny (z ~3h w v1), w tempie uczestnika.
