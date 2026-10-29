# RundfunkArr-Dokumentation

Quelle der Dokumentation unter **https://rundfunkarr.github.io/**. Die Anwendung selbst liegt in
[rundfunkarr/rundfunkarr](https://github.com/rundfunkarr/rundfunkarr).

Die Seite wird mit [VitePress](https://vitepress.dev) gebaut. Jede Markdown-Datei im
Hauptverzeichnis ist eine Seite; Navigation und Seitenleiste stehen in `.vitepress/config.mts`.
Screenshots kommen direkt aus `docs/screenshots` im Anwendungs-Repository, damit README und
Dokumentation dieselben Bilder zeigen.

```bash
npm install
npm run dev      # lokale Vorschau mit Hot Reload
npm run build    # Build nach .vitepress/dist, prüft auch tote Links
```

Änderungen auf `main` veröffentlicht der Workflow `.github/workflows/deploy.yml` auf GitHub Pages.
Dokumentation und Oberfläche sind deutsch.
