# MinimalApp

MinimalApp è una semplice applicazione Android che carica il sito [https://example.com/](https://example.com/) all’interno di una WebView, offrendo il supporto a:

- Gestione dei permessi di geolocalizzazione
- Caricamento e selezione di file/foto dal dispositivo
- Navigazione con JavaScript abilitato

---

## Caratteristiche

- **WebView full‑screen** con JavaScript e geolocalizzazione abilitati  
- **File chooser** per upload di immagini o altri file tramite WebView  
- **Richiesta runtime dei permessi** per accesso a storage e posizione  

---

## Requisiti

- Android Studio **Arctic Fox** o superiore
- SDK Android 5.0 (API Level 21) o superiore
- **AndroidX** abilitato  

---

## Permessi

L’app richiede i seguenti permessi, dichiarati in `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
```

- **Internet**: per caricare il sito web  
- **Storage**: per selezionare e caricare file/foto  
- **Location**: per consentire al sito di accedere alla geolocalizzazione  

---

## Installazione

1. **Clona** il repository:
   ```bash
   git clone https://github.com/tuo-username/minimal-app.git
   cd minimal-app
   ```
2. **Configura** il percorso dell’SDK Android in `local.properties`:
   ```properties
   sdk.dir=/percorso/alla/tuo/Android/Sdk
   ```
3. **Apri** il progetto in Android Studio e **build**.

---

## Utilizzo

All’avvio, l’app richiederà i permessi di **posizione** e **storage**. Una volta concessi:

1. Viene caricata la WebView full‑screen con `https://example.com/`  
2. Qualsiasi richiesta di file chooser (upload) sarà gestita automaticamente da `MainActivity.kt`  
3. Le richieste di geolocalizzazione dal sito verranno approvate in modo trasparente

---

## Struttura del progetto

```
.
├── app
│   ├── src
│   │   ├── main
│   │   │   ├── AndroidManifest.xml     
│   │   │   └── java/com/example/minimalapp
│   │   │       └── MainActivity.kt      
│   └── build.gradle
├── gradle.properties                    
├── local.properties                     
├── settings.gradle
├── LICENSE                              
└── README.md
```

---

## Contribuire

1. Fork del repository  
2. Crea un branch feature: `git checkout -b feature/nome-feature`  
3. Commit: `git commit -m "Aggiunta nuova feature"`  
4. Push: `git push origin feature/nome-feature`  
5. Apri una Pull Request

---

## Licenza

Questo progetto è distribuito sotto la licenza MIT. Vedi il file [LICENSE](./LICENSE).
