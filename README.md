# Esercizi

**Crea uno stile in SASS**

---

Scopo dell’esercizio è creare lo stile in SCSS per un header/hero section seguito da una piccola griglia dinamica.

* Layout full width
* Semplice navbar full width con logo e 3 link: home, about, servizi
* Headline con breve descrizione e 3 bottoni colorati per: Scopri di più, Accedi, Contattaci
* Semplici proprietà di trasformazione sui bottoni
* Background sull’intera sezione hero e un’immagine a fianco del contenuto testuale
* Semplice griglia di quattro elementi ad immagine, sfondo bianco, subito dopo la hero colorata
* Animazione per l’ingresso di tutti gli elementi della hero (fade in + discesa dall’alto di qualche px)

---

Il lavoro prevede la strutturazione dei file secondo una logica di utilizzo dinamico di variabili, partials, mixins e cicli.

Bisognerà creare un file partials per:

* Reset
* Colori
* Font
* Spaziature
* Bottoni
* Mixins generici
* Animazioni

Inseriscili in un file `style.scss` principale.
Compila e genera il file CSS.

---

* Inserisci i reset più comuni nel file corrispondente
* Colori:

  * testo: `#f4f4f4`
  * bottoni: `#0e6cff`, `#ff8700`, `#4caf50`
  * bg_hero: `#640fc5`
* Inserisci il font-family nel file corrispondente e crea delle variabili per le misure principali dei font, crea anche un mixin per title-big che userai per il titolo principale
* Nel partial di spaziature “spacings”, crea dinamicamente le classi per padding-(block|inline)-(sm|normal|md|lg|xl|xxl) e margin-(block|inline)-(sm|normal|md|lg|xl|xxl), usale quando ritieni opportuno
* Nel partial “buttons” genera dinamicamente le 3 classi dei bottoni a partire dalla lista dei colori corrispondenti

---

* Nei mixin generici creane uno chiamato “floating” in cui verranno definite: border-radius, box-shadow e bordo opzionali.
  Fai in modo di poter usare il mixin anche senza nessun argomento. Usa valori adeguati per dare un senso di “sollevamento”, tramite ombreggiatura, all’elemento che li riceverà.

  Questo mixin lo useranno:

  1. l’immagine principale della hero, con un bordo chiaro
  2. le immagini della griglia, ma con valori diversi di ombreggiatura e senza bordo.

* Sempre nei mixin generici crea un mixin “grid” che definirà una griglia flex, il numero di elementi per linea sarà determinato dal parametro in ingresso. Con un parametro diverso si avranno più o meno elementi per linea.

* Infine nel partial “animations” crea un mixin per l’animazione (fade in + discesa dall’alto di qualche px).
  Durata, punto di inizio e di fine, delay, nome, saranno parametri in ingresso per differenziare l’animazione sui diversi elementi della hero section.
  **Il “nome” dovrà sempre essere univoco per ogni utilizzo di questo mixin.**
