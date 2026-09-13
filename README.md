# Acquario smart

Pannello di controllo di un acquario da 120 litri con tre pesci rossi.

**Apri:** https://cercarelliriccardo-lab.github.io/acquario/

Temperatura, luce (cinque modi, intensità, orari automatici), filtro, manutenzione
e calendario dei lavori, tutto letto e comandato da una centralina ESP32.

## Come arriva alla vasca

- **In casa** il telefono parla direttamente con la centralina, su
  `http://acquario.local`, che serve questa stessa pagina.
- **Fuori casa** la pagina passa da un server MQTT su HiveMQ Cloud: è la
  centralina che si collega a internet, sul router non c'è nessuna porta aperta.
  La password dell'utenza del telefono si inserisce una volta nell'app e resta
  solo sul telefono: in questo repository non ce n'è nessuna.

## File

- `docs/index.html` — la pagina pubblicata. È una copia di `pagina.h` del firmware,
  estratta dalla stringa: il codice vero si modifica lì, poi si ricopia qui.
- `docs/pannello/` — rimanda al vecchio indirizzo, per le icone già salvate
  sulla schermata Home.
