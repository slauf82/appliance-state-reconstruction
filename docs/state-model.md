# Zustandsmodell

Die Automation rekonstruiert einen stabilen, nutzerrelevanten Gerätezustand aus mehreren technischen Statusquellen.

## Vereinfachtes Modell

```text
ready -> running -> finished -> ready
```

## Wichtige Regel

Der Zustand `finished` bleibt sichtbar, bis die Tür geöffnet wird. Dadurch geht die wichtigste Nutzerinformation nicht verloren, auch wenn das Gerät oder die Cloud-Integration den Status frühzeitig zurücksetzt.

## Warum das interessant ist

Das Projekt zeigt typische Konzepte aus ereignisgetriebenen Systemen:

- verzögerte Ereignisse
- unvollständige Datenquellen
- Recovery nach Neustarts
- persistierte logische Zustände
- Synchronisation zwischen technischem und fachlichem Zustand
