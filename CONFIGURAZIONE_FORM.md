# 📧 Configurazione Form di Contatto

## ✅ Cosa ho fatto

Ho configurato il form per usare **Netlify Forms**, il servizio integrato di Netlify che gestisce automaticamente l'invio delle email.

## 📍 Dove arrivano i messaggi

Quando qualcuno compila e invia il form, i dati arrivano in **due posti**:

### 1. Dashboard Netlify
- Vai su https://app.netlify.com/
- Seleziona il tuo sito
- Vai su **Forms** nel menu laterale
- Vedrai tutti i messaggi inviati con tutti i dati (nome, email, telefono, messaggio)

### 2. Email (da configurare)
Per ricevere i messaggi via email, devi configurare le notifiche:

1. Vai su **Site settings** → **Forms** → **Form notifications**
2. Clicca su **Add notification**
3. Scegli **Email notification**
4. Inserisci l'email dove vuoi ricevere i messaggi (es: info@kingfx.eu)
5. Salva

## 🔧 Come funziona

Il form è configurato con:
- ✅ **Netlify Forms** integrato (`data-netlify="true"`)
- ✅ **Honeypot** per protezione spam (campo nascosto)
- ✅ **Redirect automatico** dopo l'invio
- ✅ **Messaggio di conferma** per l'utente

## 📝 Dati raccolti

Il form raccoglie:
- Nome e Cognome (obbligatorio)
- Email (obbligatorio)
- Telefono (opzionale)
- Messaggio (obbligatorio)
- Consenso privacy (obbligatorio)

## 🚀 Prossimi passi

1. **Fai commit e push** delle modifiche su GitHub
2. **Netlify farà il deploy** automaticamente
3. **Configura le notifiche email** nel dashboard Netlify (opzionale ma consigliato)
4. **Testa il form** compilando e inviando un messaggio di prova

## 💡 Note importanti

- **Netlify Forms è gratuito** fino a 100 invii al mese (piano gratuito)
- I messaggi sono salvati nel dashboard Netlify per 30 giorni (piano gratuito)
- Puoi esportare i dati in CSV dal dashboard
- Le notifiche email sono immediate

## 🔒 Privacy e Sicurezza

- Il form include un campo honeypot per proteggere dallo spam
- I dati sono gestiti da Netlify in conformità con GDPR
- L'utente deve accettare l'informativa sulla privacy prima di inviare

