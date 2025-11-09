# Configurazione Netlify per King FX

## Struttura del Sito

Il sito è organizzato con le seguenti route:

- **Root (`/`)**: Reindirizza automaticamente a `/home`
- **Home Page (`/home`)**: Home page principale di King FX Financed
- **Landing Page (`/landing`)**: Landing page per KING EA

## Configurazione Netlify

### 1. Impostazioni Build in Netlify

Nel pannello di controllo Netlify:

1. Vai su **Site settings** → **Build & deploy** → **Build settings**
2. **Publish directory**: Lascia vuoto o imposta a `.` (root del repository)
3. **Build command**: Lascia vuoto (non serve build per siti statici)

### 2. File di Configurazione

Il file `netlify.toml` nella root del repository contiene:
- Redirects per `/landing` → `/Landing KingFX/`
- Redirects per `/home` → `/Home KingFX/`
- Redirect della root `/` → `/Home KingFX/index.html`
- Headers per sicurezza e cache

### 3. Deploy

Dopo aver fatto push su GitHub:

1. Netlify rileverà automaticamente il nuovo commit
2. Il deploy partirà automaticamente
3. I redirects configurati in `netlify.toml` saranno attivi

### 4. Verifica

Dopo il deploy, verifica che funzionino:

- ✅ `https://portal.kingfx.eu/` → Reindirizza a `/home`
- ✅ `https://portal.kingfx.eu/home` → Mostra Home KingFX
- ✅ `https://portal.kingfx.eu/landing` → Mostra Landing KingFX

## Struttura File

```
/
├── index.html              # Pagina root (reindirizza a /home)
├── netlify.toml           # Configurazione Netlify
├── Landing KingFX/        # Landing page KING EA
│   ├── index.html
│   ├── styles.css
│   └── ... (immagini e risorse)
└── Home KingFX/           # Home page principale
    ├── index.html
    ├── styles.css
    └── ... (immagini e risorse)
```

## Note Importanti

- I percorsi relativi nelle immagini e CSS funzionano correttamente perché Netlify serve i file dalla loro posizione originale
- Il file `netlify.toml` gestisce i redirects senza modificare la struttura delle cartelle
- Se vuoi cambiare quale pagina viene mostrata alla root, modifica il redirect in `netlify.toml`

## Troubleshooting

Se i redirects non funzionano:

1. Verifica che il file `netlify.toml` sia nella root del repository
2. Controlla i log di deploy in Netlify per errori
3. Assicurati che i percorsi delle cartelle siano corretti (con spazi: "Landing KingFX" e "Home KingFX")
4. Prova a fare un nuovo deploy dopo aver verificato la configurazione

