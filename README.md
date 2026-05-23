# ⚡ Strømpriser Norge – Live Dashboard

Et live strømpris-dashboard for Norges fem prissoner, bygget med ren HTML/CSS/JS.

## 🌐 Live demo
Tilgjengelig på GitHub Pages:
`https://<ditt-brukernavn>.github.io/strompriser/`

## 📊 Funksjoner

- Live henting av spotpriser fra [hvakosterstrommen.no](https://www.hvakosterstrommen.no/strompris-api)
- Viser alle 5 norske prissoner: NO1 · NO2 · NO3 · NO4 · NO5
- Velg enkeltssoner eller alle
- **I dag**-visning: timepris time for time
- **7 dager**-visning: historisk kurve
- Automatisk oppdatering hvert 5. minutt
- Infokort med nåpris, høy og lav per sone
- Interaktiv tooltip ved hover

## 🗂️ Filstruktur

```
strompriser/
├── index.html   # Hele applikasjonen (én fil)
└── README.md    # Denne filen
```

## 🚀 Slik kjører du det lokalt

```bash
# Klon repoet
git clone https://github.com/<brukernavn>/strompriser.git
cd strompriser

# Start en lokal server (Python)
python -m http.server 8080

# Åpne i nettleser
# http://localhost:8080
```

> **Merk:** Filen må kjøres via en webserver (ikke direkte som `file://`) fordi den henter data fra et eksternt API.

## 🌍 Deploy til GitHub Pages

1. Push repoet til GitHub
2. Gå til **Settings → Pages**
3. Velg branch `main`, mappe `/` (root)
4. Klikk **Save** — siden er live på noen sekunder

## 📡 Datakilde

Data leveres av [hvakosterstrommen.no](https://www.hvakosterstrommen.no) sitt åpne og gratis API:

```
GET https://www.hvakosterstrommen.no/api/v1/prices/{år}/{mm}-{dd}_{sone}.json
```

Priser er spotpris ekskl. MVA og nettleie.

## 📄 Lisens

MIT – fri til bruk og viderebygging.
