# King FX Financed - Sito Web

Sito web per King FX Financed con landing page e home page.

## 📁 Struttura del Progetto

```
SITO KINGFX/
├── index.html          # Pagina root (reindirizza a /home)
├── netlify.toml        # Configurazione Netlify
├── _redirects          # File redirects per Netlify
├── landing/            # Landing page KING EA
│   ├── index.html
│   ├── styles.css
│   ├── Risultati/      # Immagini dei risultati
│   └── ... (immagini e risorse)
└── home/               # Home page principale
    ├── index.html
    ├── styles.css
    └── ... (immagini e risorse)
```

## 🌐 URL del Sito

- **Root**: `https://portal.kingfx.eu/` → Reindirizza a `/home`
- **Home Page**: `https://portal.kingfx.eu/home`
- **Landing Page**: `https://portal.kingfx.eu/landing`

## 🚀 Deploy

Il sito è configurato per il deploy automatico su Netlify tramite GitHub.

### Configurazione Netlify

- **Publish directory**: `.` (root)
- **Build command**: (vuoto - sito statico)
- **Redirects**: Gestiti tramite `_redirects` e `netlify.toml`

## 📝 Note

- Le cartelle `landing/` e `home/` contengono le rispettive pagine
- I file di configurazione (`netlify.toml` e `_redirects`) gestiscono il routing
- Tutte le immagini e risorse sono nelle rispettive cartelle

