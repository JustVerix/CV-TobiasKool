# Tobias Booms — Profielpagina

Persoonlijke profielpagina voor de HvA-opleiding HBO-ICT (Student Wrapped, AA2-1 / OR3-1). De pagina stelt mezelf voor aan docenten en medestudenten en is gebouwd met HTML en CSS (zonder JavaScript).

---

## Inhoud

- [Projectstructuur](#projectstructuur)
- [Pagina's](#paginas)
- [Vormgeving](#vormgeving)
- [Afbeeldingen](#afbeeldingen)
- [Externe content](#externe-content)
- [Installatie](#installatie)
- [Contact](#contact)

---

## Projectstructuur

```
Profielpagina - Tobias Booms/
├── index.html              ← Homepage (voorstel, profielfoto)
├── design.css              ← Eén gedeeld stylesheet voor alle pagina's
├── README.md               ← Dit document
├── aantekening.md          ← Verouderd testbestand, kan verwijderd worden
├── images/                 ← 11 afbeeldingen
└── html/                   ← 6 sectiepagina's
    ├── helldivers2.html    ← Mijn favoriete spel
    ├── muziekgenres.html   ← Mijn muziekgenres
    ├── gitaar.html         ← Gitaar spelen
    ├── katten.html         ← Mijn katten
    ├── eten.html           ← Mijn favoriete eten
    └── game-uren.html      ← Mijn game-uren
```

## Pagina's

De site telt 7 pagina's: de homepage plus zes sectiepagina's. Elke pagina heeft dezelfde opbouw:

- **Header** — profielfoto (rond), naam (`Tobias Booms`) en een per-pagina tekstregel. De tekstregel staat rechtsboven in de header (`margin-left: auto` in CSS).
- **Navigatie** — identiek op alle pagina's. Elke link heeft de klasse `nav-buttons`; de huidige pagina wordt gemarkeerd met `class="nav-buttons active"`.
- **Sectie** — twee kolommen naast elkaar: tekst links (`.text-container`) en afbeeldingen rechts (`.image-container`).
- **Footer** — contactgegevens.

## Vormgeving

De styling staat volledig in `design.css`, gedeeld door alle pagina's. Kleuren worden beheerd via variabelen in `:root`:

| Variabele | Waarde | Functie |
|---|---|---|
| `--color-background` | `#000000` | Achtergrond |
| `--color-text` | `#6ad003` | Hoofdtekst (groen, terminalstijl) |
| `--color-green` | `#274b0e` | Randen, navigatiebalk, tekstvakken |
| `--color-light-green` | `#3e6b1a` | Nav-knoppen (`nav-buttons`) |
| `--color-black` | `#000000` | Actieve nav-knop, foto-rand, footer |

De vormgeving is een donkergroene, terminalachtige stijl:

- Lettertype `mono` (mono-spaced).
- Elk tekstblok in een sectie begint met de prompt `~ ) `, toegevoegd via `.section-text::before` in CSS.
- `body` heeft `min-height: 100vh` en `display: flex; flex-direction: column`; `main` heeft `flex: 1`. Hierdoor blijft de footer altijd onderaan het scherm, ongeacht de inhoudshoogte van de pagina.
- Afbeeldingen hebben een hover-effect (`transform: scale(1.05)`) met een overgang van 0.3s.

## Afbeeldingen

De map `images/` bevat 11 bestanden, waaronder:

- `pfp.png` — profielfoto, gebruikt in de header van alle 7 pagina's
- `felixdecat.jpg`, `jippiedecat.jpg`, `felix_en_jippie.jpg` — de katten Felix en Jippie
- `helldivers_screenshot.jpg` — screenshot van Helldivers 2
- `black_sabbath.jpg` — albumhoes, gebruikt op de muziekgenres-pagina
- `steam_library.png` — Steam-bibliotheek, gebruikt op de game-uren-pagina
- `music.jpg`, `tobias_op_podium_muziek.jpg` — gitaar-gerelateerde foto's
- `sushi.jpg` — sushifoto, gebruikt op de eten-pagina
- `tobiasmethelmenvrienden.jpg` — persoonlijke foto op de homepage

## Externe content

- Op `html/helldivers2.html` staat een Steam-widget (iframe) van Helldivers 2, ingesloten via `https://store.steampowered.com/widget/553850/`.
- Op `html/game-uren.html` staat een link naar het [SteamTime-profiel](https://steamtime.info/s/76561199221961316).

## Installatie

1. Kloon de repository of download de bestanden.
2. Open `index.html` in een browser.

Er is geen buildstap of package manager nodig; de site draait rechtstreeks vanuit de bestanden.

## Contact

Tobias Booms — [tobias.booms@hva.nl](mailto:tobias.booms@hva.nl)