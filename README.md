<h1 align="center"><b>EasyTube</b> per Android</h1>

<p align="center">Client YouTube nativo, senza pubblicità, con SponsorBlock e Return YouTube Dislike.</p>

---

## Cos'è

**EasyTube** per Android è un client YouTube leggero e privato, **rebrand di
[Tubular](https://github.com/polymorphicshade/Tubular)** — a sua volta fork di
**[NewPipe](https://github.com/TeamNewPipe/NewPipe)** — che integra
**[SponsorBlock](https://sponsor.ajay.app/)** e
**[ReturnYouTubeDislike](https://www.returnyoutubedislike.com/)**.

È la versione **nativa Android** del progetto EasyTube (originariamente
un'estensione per Firefox), pensata per girare in modo indipendente, senza
dipendere dalla revisione di store di terze parti.

## Funzionalità (ereditate da NewPipe/Tubular)

- **Senza pubblicità** — non usa una WebView né le API ufficiali, estrae i dati da YouTube.
- **SponsorBlock** — salta automaticamente sponsor, intro, outro, ecc.
- **Return YouTube Dislike** — mostra i "non mi piace".
- **Niente login Google necessario** — iscrizioni e cronologia gestite localmente.
- Riproduzione in background e in popup, download, niente tracciamento.

## Modifiche rispetto a Tubular (upstream)

Questo fork è puramente un **rebrand**; la logica dell'app è quella di Tubular.
Modifiche applicate:

| Cosa | Da (Tubular) | A (EasyTube) |
|---|---|---|
| `applicationId` | `org.polymorphicshade.tubular` | `com.dom19.easytube` |
| Nome app | Tubular | EasyTube |
| Icona launcher | icona Tubular | logo EasyTube |
| Sfondo icona adattiva | `#CD201F` | `#15151F` |

> Il *namespace* del codice resta `org.schabi.newpipe` (rinominarlo richiederebbe
> di rifattorizzare migliaia di riferimenti; in Android `applicationId` ≠ `namespace`
> è del tutto lecito).

Base: Tubular **v0.28.4**.

## Build

Serve **JDK 17** e l'**Android SDK** (platform `android-36`, build-tools `36.0.0`).

```bash
./gradlew assembleDebug
# APK in: app/build/outputs/apk/debug/app-debug.apk
```

L'APK di debug è firmato con la chiave di debug di Android (va bene per il
sideload su un proprio dispositivo, non per la distribuzione pubblica).

## Crediti e licenza

EasyTube non sarebbe possibile senza il lavoro di:

- **[NewPipe](https://github.com/TeamNewPipe/NewPipe)** — © NewPipe e.V. e contributori
- **[Tubular](https://github.com/polymorphicshade/Tubular)** — © polymorphicshade
- **[SponsorBlock](https://github.com/ajayyy/SponsorBlock)** e **[Return YouTube Dislike](https://github.com/Anarios/return-youtube-dislike)**

[![GNU GPLv3](https://www.gnu.org/graphics/gplv3-127x51.png)](https://www.gnu.org/licenses/gpl-3.0.en.html)

Distribuito sotto **GNU GPL v3.0** (vedi [LICENSE](LICENSE)), come i progetti da
cui deriva. NewPipe e Tubular **non** sono affiliati a questo rebrand e non lo
supportano. "YouTube" è un marchio di Google LLC; questo progetto non è
affiliato né approvato da Google.
