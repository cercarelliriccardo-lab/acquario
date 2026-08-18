# Acquario smart — app

Cruscotto dell'acquario da 120 litri: scena 3D della vasca in tempo reale
(Three.js) con i componenti che si toccano per vederne dati e comandi.

Una pagina sola, `index.html`, senza passaggio di compilazione: si apre servendola
via http.

**I valori mostrati sono ancora simulati**: il firmware ESP32 che leggerà sonda,
striscia LED e relè non esiste ancora. Quando ci sarà, il gancio della
temperatura è `TEMPERATURA.valore`.

## Modelli 3D

- pesci "Veiltail goldfish" e "Jikin goldfish" di **somitsu** (Sketchfab),
  licenza [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- sasso: fotoscansione da Sketchfab, licenza CC BY 4.0
- piante: modellate per questo progetto
- pesce di ripiego (`pesce-rosso.obj`): generato con Meshy, orientato e colorato
  dallo script del progetto

## Prove in locale

```
python -m http.server 8000
```

poi `http://localhost:8000`. Con il doppio click non parte: i browser bloccano i
moduli JavaScript nelle pagine aperte come file locale.
