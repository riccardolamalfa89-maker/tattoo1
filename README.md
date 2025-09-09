# TattooPro — Blueprint CORRETTO (rootDir) per Render

Questa versione corregge gli errori alle righe 17 e 50 (causati da `repoPath`):
Render si aspetta **rootDir** per indicare la sotto-cartella del monorepo.

## Passi
1) Carica questo `render.yaml` nel tuo repo GitHub (sostituisci quello precedente).
2) Su Render → **Blueprint Instance** → **Sync/Apply**.
3) Attendi la build (5–10 min).
4) Apri il servizio **tattoopro-web** → **Open in Browser**.

### Importante (API URL)
Il frontend prende l’URL dell’API da `NEXT_PUBLIC_API_URL`, che con il blueprint punta alla **base** dell’API.  
Se nel tuo codice non è stata applicata la patch che aggiunge automaticamente `'/v1'`, fai così:

- Vai su **tattoopro-web** → **Environment**  
- modifica `NEXT_PUBLIC_API_URL` in:
```
<URL_pubblico_API>/v1
```
(es. `https://tattoopro-api-xxxxx.onrender.com/v1`)
- **Save** → **Deploy**.

### Credenziali demo
```
user: owner@example.com
password: changeme
```

Se Render segnala errori, copia qui il testo dell’errore e il servizio (API/Web) interessato: ti do la fix mirata.