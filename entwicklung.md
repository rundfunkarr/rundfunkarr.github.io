# Entwicklung

Wie man beiträgt, steht ausführlich in der
[CONTRIBUTING.md](https://github.com/rundfunkarr/rundfunkarr/blob/main/CONTRIBUTING.md). Kurz:

```bash
npm install
npx prisma migrate dev

npm run dev          # Entwicklungsserver mit Hot Reload
npm run lint         # ESLint
npm run typecheck    # TypeScript
npm run test         # Vitest
npm run db:migrate   # Datenbank-Migration erstellen
```

## Projektstruktur

```
src/
├── app/               # Next.js App Router
│   ├── api/           # API Routes
│   │   ├── newznab/   # Indexer-API (Newznab)
│   │   ├── settings/  # Settings-API
│   │   └── route.ts   # Downloader-API (SABnzbd)
│   ├── settings/      # Einstellungen
│   ├── setup/         # Setup-Wizard
│   ├── search/        # Suche
│   └── downloads/     # Downloads
├── components/        # React-Komponenten
├── contexts/          # React Context
├── services/          # Geschäftslogik (Mediathek-Suche und Regelabgleich, TVDB, TMDB, Newznab)
├── server/            # Nur serverseitig (Download-Manager, FFmpeg, Filmlisten-Index)
└── lib/               # Hilfsfunktionen (Prisma, Caches, Settings)
data/
├── shows.json         # Lokale Show-Datenbank
└── rulesets.json      # Matching-Rulesets
```

## Diese Dokumentation

Die Seite liegt im Repository
[rundfunkarr/rundfunkarr.github.io](https://github.com/rundfunkarr/rundfunkarr.github.io) und wird
mit [VitePress](https://vitepress.dev) gebaut. Änderungen auf `main` veröffentlicht ein
GitHub-Actions-Workflow automatisch. Korrekturen gern als Pull Request dort; der Link „Diese Seite
auf GitHub bearbeiten“ unten auf jeder Seite führt direkt zur passenden Datei.

```bash
npm install
npm run dev
```

## Credits

- [PCJones/MediathekArr](https://github.com/PCJones/MediathekArr): ursprüngliche .NET-Implementierung
- [MediathekViewWeb](https://github.com/mediathekview/mediathekviewweb): Mediathek-API
- [TheTVDB](https://thetvdb.com) und [TMDB](https://www.themoviedb.org): Metadaten-APIs
