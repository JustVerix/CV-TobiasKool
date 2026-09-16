# Tobias Kool — CV

Online cv van Tobias Kool, gebouwd met HTML en CSS (zonder JavaScript). De site heeft een donkergroene, terminalachtige uitstraling en is opgebouwd uit zeven pagina's.

---

## Inhoud

- [Projectstructuur](#projectstructuur)
- [Pagina's](#paginas)
- [Vormgeving](#vormgeving)
- [Contact](#contact)

---

## Projectstructuur

```
CV-TobiasKool/
├── index.html              ← Profiel (homepage)
├── design.css              ← Eén gedeeld stylesheet voor alle pagina's
├── README.md               ← Dit document
├── aantekening.md          ← Verouderd testbestand, kan verwijderd worden
├── images/                 ← Afbeeldingen (o.a. profielfoto)
├── cv/                     ← Downloadbare cv (PDF en Word)
└── html/                   ← 6 cv-sectiepagina's
    ├── werkervaring.html   ← Werkervaring
    ├── opleiding.html      ← Opleiding
    ├── vaardigheden.html   ← Vaardigheden
    ├── hobbies.html        ← Hobbies
    ├── talen.html          ← Talen
    └── contact.html        ← Contactgegevens
```

## Pagina's

De site telt 7 pagina's: de homepage (profiel) plus zes sectiepagina's. Elke pagina heeft dezelfde opbouw:

- **Header** — profielfoto (rond), naam (`Tobias Kool`) en een per-pagina tekstregel. De tekstregel staat rechtsboven in de header (`margin-left: auto` in CSS).
- **Navigatie** — identiek op alle pagina's. Elke link heeft de klasse `nav-buttons`; de huidige pagina wordt gemarkeerd met `class="nav-buttons active"`.
- **Sectie** — cv-inhoud in tekstblokken (`.section-text`).
- **Footer** — contactgegevens.

## Vormgeving

De styling staat volledig in `design.css`, gedeeld door alle pagina's. Kleuren worden beheerd via variabelen in `:root`:

| Variabele | Waarde | Functie |
|---|---|---|
| `--color-background` | `#000000` | Achtergrond |
| `--color-text` | `#6ad003` | Hoofdtekst (groen, terminalstijl) |
| `--color-green` | `#274b0e` | Randen, navigatiebalk, tekstvakken |
| `--color-light-green` | `#3e6b1a` | Nav-knoppen (`nav-buttons`) |
| `--color-black` | `#000000` | Actieve nav-knop, footer |

De vormgeving is een donkergroene, terminalachtige stijl:

- Lettertype `mono` (mono-spaced).
- Elk tekstblok begint met de prompt `~ ) `, toegevoegd via `.section-text::before` in CSS.
- `body` heeft `min-height: 100vh` en `display: flex; flex-direction: column`; `main` heeft `flex: 1`, zodat de footer altijd onderaan staat.

## Contact

Tobias Kool — [tobiasbooms@gmail.com](mailto:tobiasbooms@gmail.com) — (+31) 06 83989923
