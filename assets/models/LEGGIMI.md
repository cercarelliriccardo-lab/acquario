# Modelli 3D

## Rocce (in lavorazione)

Man mano che i sassi vengono modellati, vanno messi qui con questi nomi esatti:

| file | posto in vasca |
|---|---|
| `roccia-a.obj` + `roccia-a.mtl` | lastra, al centro-destra |
| `roccia-b.obj` + `roccia-b.mtl` | piccola, a destra |
| `roccia-c.obj` + `roccia-c.mtl` | tonda, davanti |

**Servono tutti e due i file**, con lo stesso nome: l'`.obj` contiene la
geometria, l'`.mtl` solo la scheda del materiale. Da solo, l'`.mtl` non fa
vedere niente.

Se manca l'`.mtl` il modello si carica lo stesso, grigio. Se manca l'`.obj`
resta il sasso costruito a codice e la scena funziona uguale.

**Le misure non contano.** Il registro in `index.html` (elenco `ARREDO`)
dichiara quanto dev'essere grande ogni sasso in vasca e ci pensa il caricatore
a scalarlo, misurandolo sul lato più lungo. Serve solo che le **proporzioni**
siano giuste. Anche l'origine non conta: la base viene appoggiata sul fondo da
sola.

---

# Modello 3D dei pesci

Qui va il file **`comet-goldfish.glb`**.

## Da dove si scarica

<https://sketchfab.com/3d-models/comet-goldfish-5adcbf784df540a0b46dae8950bd3ec6>

Autore: **somitsu**. Serve un account Sketchfab (gratuito) per scaricare — il
tasto *Download 3D Model* compare solo da loggati. Scegliere il formato
**glTF (.glb)**, non FBX né USDZ: `.glb` è l'unico che Three.js legge nativamente
e contiene già dentro texture, scheletro e animazione di nuoto.

Se l'archivio scaricato è uno `.zip`, estrarre il `.glb` e rinominarlo
`comet-goldfish.glb`.

## Licenza — attenzione, va rispettata

**CC Attribution 4.0 (CC BY 4.0)**: si può usare e modificare anche in un
progetto pubblico, **a patto di citare l'autore**. La citazione è già nell'app,
in fondo allo schermo:

> "Comet goldfish" di somitsu (Sketchfab) — licenza CC BY 4.0

Se il file viene sostituito con un altro modello, va cambiata anche quella
scritta (`const CREDITI` in `app/index.html`) e ricontrollata la licenza del
nuovo modello: su Sketchfab non sono tutte uguali, alcune vietano il riuso.

## Se il file non c'è

Non succede niente di grave: `index.html` se ne accorge e disegna dei pesci
costruiti a codice, con la stessa forma e lo stesso nuoto. La scena funziona
comunque, cambia solo il livello di dettaglio.

## Nota sui percorsi locali

Aprendo `index.html` con doppio click (`file://`) il browser **blocca** il
caricamento del `.glb` per motivi di sicurezza, e si vedono i pesci procedurali
anche se il file c'è. Per vedere il modello vero serve un server locale:

```bash
python -m http.server 8000
```

e poi aprire <http://localhost:8000/app/>.
