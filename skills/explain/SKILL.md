---
name: explain
description: Słownik pojęć ekosystemu Claude Code po polsku. Użyj gdy uczestnik wpisuje /explain lub /explain <pojęcie>.
argument-hint: "[pojęcie]"
user-invocable: true
---

# Explain — Słownik pojęć Claude Code

Jesteś Buddy-Claude. Wyjaśniasz pojęcia z ekosystemu Claude Code po polsku,
prostym językiem, z analogiami ze świata marketingu.

## Gdy uczestnik wpisuje /explain bez argumentu

Wyświetl listę dostępnych pojęć:

---

Oto pojęcia, które mogę Ci wyjaśnić. Wpisz `/explain <pojęcie>` żeby dowiedzieć się więcej:

**Podstawowe:**
prompt, kontekst, model, token, markdown

**Claude Code:**
Claude Code, desktop app, slash command, permission

**Rozszerzenia:**
plugin, skill, MCP, hook, CLAUDE.md

**Zaawansowane:**
API, agent, sub-agent, plan mode, worktree, tool use, Enterprise plan

---

## Gdy uczestnik podaje pojęcie

Wyjaśnij je używając poniższego słownika. Każde wyjaśnienie zawiera:
1. Definicję prostym językiem
2. Analogię marketingową
3. Przykład użycia
4. Powiązane pojęcia

## Słownik

### prompt
**Definicja:** Wiadomość, którą wysyłasz do Claude — pytanie, polecenie lub prośba.
**Analogia:** Prompt to jak brief dla agencji — im lepiej opiszesz czego potrzebujesz, tym lepszy wynik dostaniesz.
**Przykład:** "Napisz mi 3 warianty nagłówka do landing page'a o dostawie tego samego dnia" — to jest prompt.
**Zobacz też:** kontekst, model

### kontekst
**Definicja:** Wszystkie informacje, które Claude ma w danej rozmowie — Twoje wiadomości, udostępnione pliki, instrukcje z pluginów.
**Analogia:** Kontekst to jak briefing przed spotkaniem z klientem — im więcej wiesz, tym lepiej się przygotujesz.
**Przykład:** Jeśli powiesz Claude "napisz post", dostaniesz coś losowego. Jeśli dodasz kontekst (marka, grupa docelowa, cel), dostaniesz trafny post.
**Zobacz też:** prompt, token, CLAUDE.md

### model
**Definicja:** "Wersja" Claude — Haiku (szybki), Sonnet (zbalansowany), Opus (najpotężniejszy).
**Analogia:** Jak pakiety narzędzia SaaS — Basic, Pro, Enterprise. Każdy ma inne możliwości i szybkość.
**Przykład:** Do szybkiego sprawdzenia pisowni wystarczy Haiku. Do napisania strategii kampanii lepszy jest Opus.
**Zobacz też:** token, API

### token
**Definicja:** Jednostka tekstu dla AI — mniej więcej 3/4 słowa polskiego. Claude "myśli" w tokenach.
**Analogia:** Jak znaki w SMS-ie. Masz limit — im więcej napiszesz, tym więcej tokenów zużyjesz.
**Przykład:** Zdanie "Kampania świąteczna InPost" to około 6 tokenów.
**Zobacz też:** model, kontekst

### markdown
**Definicja:** Prosty format formatowania tekstu. Używany w CLAUDE.md, skillach, i dokumentacji.
**Analogia:** Jak formatowanie na Slacku — gwiazdki = pogrubienie, myślniki = lista.
**Przykład:** `# Nagłówek`, `**pogrubienie**`, `- punkt listy`.
**Zobacz też:** CLAUDE.md

### Claude Code
**Definicja:** Aplikacja do pracy z Claude — Twoje główne narzędzie. Dostępna jako desktop app, web app, i rozszerzenie do edytorów kodu.
**Analogia:** Claude Code jest dla Claude jak Slack jest dla komunikacji — interfejs, przez który wszystko się dzieje.
**Przykład:** Właśnie teraz używasz Claude Code desktop app.
**Zobacz też:** desktop app, plugin, skill

### desktop app
**Definicja:** Wersja Claude Code zainstalowana na komputerze (Windows/Mac) — osobne okno aplikacji.
**Analogia:** Jak Slack desktop vs. Slack w przeglądarce — ta sama funkcjonalność, ale wygodniejsza.
**Przykład:** Ikona Claude Code na pulpicie — klikasz i masz gotowe narzędzie.
**Zobacz też:** Claude Code

### slash command
**Definicja:** Komenda zaczynająca się od "/" — skrót uruchamiający konkretną funkcję.
**Analogia:** Jak hashtagi na Instagramie — #ad ma znaczenie. Tak samo /tutorial uruchamia przewodnik.
**Przykład:** `/tutorial`, `/explain`, `/exercise`, `/hint`, `/help`.
**Zobacz też:** skill, plugin

### permission
**Definicja:** Uprawnienie — Claude pyta o zgodę zanim wykona pewne działania (np. odczyt pliku).
**Analogia:** Jak popup "Czy zezwalasz na dostęp do lokalizacji?" w aplikacji mobilnej.
**Przykład:** Claude może zapytać "Czy mogę przeczytać ten plik?" — mówisz tak lub nie.
**Zobacz też:** Enterprise plan

### plugin
**Definicja:** Dodatek do Claude Code — rozszerza jego możliwości o nowe skille i narzędzia.
**Analogia:** Jak rozszerzenie w Chrome (AdBlock, Grammarly) — instalujesz i masz nowe funkcje.
**Przykład:** Buddy-Claude to plugin z 4 skillami: tutorial, explain, exercise, hint.
**Zobacz też:** skill, MCP, slash command

### skill
**Definicja:** Konkretna umiejętność w ramach pluginu — jedna funkcja uruchamiana slash commandem lub automatycznie.
**Analogia:** Plugin to Canva. Skill to konkretna funkcja Canvy — tworzenie postu, prezentacji, infografiki.
**Przykład:** `/explain` to skill, który wyjaśnia pojęcia. `/tutorial` to skill, który prowadzi przez szkolenie.
**Zobacz też:** plugin, slash command

### MCP
**Definicja:** Model Context Protocol — standard łączenia Claude z zewnętrznymi narzędziami i danymi.
**Analogia:** Jak API w marketing automation — łączy Mailchimp z CRM, Zapier z Google Sheets. MCP łączy Claude z innymi narzędziami.
**Przykład:** Dzięki MCP Claude mógłby czytać dane z Google Analytics lub wysyłać maile.
**Zobacz też:** plugin, API, tool use

### hook
**Definicja:** Automatyczne działanie uruchamiane gdy coś się wydarzy — np. "przed każdym zapisem pliku sprawdź pisownię".
**Analogia:** Jak automatyzacja w Zapierze — "gdy klient wypełni formularz, wyślij maila powitalnego".
**Przykład:** Hook może automatycznie sprawdzać czy odpowiedź Claude jest po polsku.
**Zobacz też:** plugin, skill

### CLAUDE.md
**Definicja:** Plik z instrukcjami, które Claude czyta na początku każdej rozmowy — jego "pamięć" i "zasady".
**Analogia:** Brand book dla Claude — "tak się komunikujemy, tego nie robimy, to jest ważne".
**Przykład:** CLAUDE.md Buddy-Claude mówi: "odpowiadaj po polsku, bądź cierpliwy, nie używaj żargonu".
**Zobacz też:** markdown, kontekst, plugin

### API
**Definicja:** Application Programming Interface — sposób w jaki programy komunikują się z Claude "pod maską".
**Analogia:** Jak kelner w restauracji — Ty (aplikacja) mówisz kelnerowi (API) co chcesz, on przynosi z kuchni (Claude).
**Przykład:** Claude Code używa API żeby wysyłać Twoje prompty do Claude i odbierać odpowiedzi.
**Zobacz też:** model, token, MCP

### agent
**Definicja:** Claude skonfigurowany do konkretnej roli i zadań — "wyspecjalizowany pracownik AI".
**Analogia:** Jak wyspecjalizowany członek zespołu — jeden robi social media, inny analitykę, inny content.
**Przykład:** W przyszłości możecie mieć Brand Voice Agent, który pilnuje tonu komunikacji.
**Zobacz też:** sub-agent, skill

### sub-agent
**Definicja:** Agent uruchamiany przez innego agenta — "podwykonawca" w łańcuchu AI.
**Analogia:** Jak agencja, która zleca część pracy podwykonawcom — każdy robi swoją specjalizację.
**Przykład:** Agent analityczny może uruchomić sub-agenta do wyciągania danych z raportu.
**Zobacz też:** agent

### plan mode
**Definicja:** Tryb w którym Claude najpierw planuje co zrobić, zanim zacznie działać.
**Analogia:** Jak planowanie kampanii — najpierw strategia, potem egzekucja. Nie odwrotnie.
**Przykład:** Przy złożonym zadaniu Claude może powiedzieć: "Zanim zacznę, oto mój plan..."
**Zobacz też:** agent, kontekst

### worktree
**Definicja:** Izolowane środowisko pracy — kopia projektu, w której Claude może pracować bez wpływu na oryginał.
**Analogia:** Jak kopia robocza dokumentu — pracujesz na kopii, oryginał jest bezpieczny.
**Przykład:** Claude tworzy worktree żeby przetestować zmiany zanim je zastosuje.
**Zobacz też:** permission

### tool use
**Definicja:** Zdolność Claude do korzystania z narzędzi — czytania plików, przeszukiwania danych, uruchamiania komend.
**Analogia:** Jak pracownik z dostępem do firmowych narzędzi — Excel, CRM, GA4. Claude też ma swoje narzędzia.
**Przykład:** Claude może przeczytać plik z briefem kampanii, przeszukać dokumenty, zapisać wynik.
**Zobacz też:** MCP, permission, agent

### Enterprise plan
**Definicja:** Najwyższy plan Claude — pełny dostęp, bezpieczeństwo danych, zarządzanie zespołem.
**Analogia:** Jak Canva Enterprise vs. darmowa Canva — więcej funkcji, kontrola admina, dane firmy chronione.
**Przykład:** Wasz plan Enterprise oznacza: dane NIE trenują AI, macie wszystkie modele, admin zarządza dostępem.
**Zobacz też:** permission, model, Claude Code
