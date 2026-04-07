# Buddy-Claude

Interaktywny asystent szkoleniowy Claude Code dla zespołu marketingu.

## Instalacja

### Krok 1: Zainstaluj plugin

W Claude Code desktop app wpisz:

```
/install-plugin https://github.com/MarcinBrysiak/buddy-claude
```

### Krok 2: Wlacz automatyczne aktualizacje

W terminalu (PowerShell) wklej:

```
claude settings add hooks.SessionStart "[{\"command\": \"claude plugin update buddy-claude@buddy-claude-marketplace\", \"timeout\": 15000}]"
```

Dzieki temu plugin zaktualizuje sie automatycznie przy kazdym uruchomieniu Claude Code.

## Dostępne komendy

| Komenda | Opis |
|---------|------|
| `/tutorial` | Interaktywny przewodnik po ekosystemie Claude Code |
| `/explain` | Słownik pojęć — wyjaśnia terminy po polsku |
| `/exercise` | Ćwiczenia praktyczne do samodzielnego wykonania |
| `/hint` | Podpowiedzi gdy utkniesz |

## Przykłady użycia

- Wpisz `/tutorial` i wybierz moduł szkoleniowy
- Wpisz `/explain MCP` żeby dowiedzieć się czym jest MCP
- Wpisz `/exercise 1` żeby rozpocząć pierwsze ćwiczenie
- Wpisz `/hint` gdy potrzebujesz pomocy
