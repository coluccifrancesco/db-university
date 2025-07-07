Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:

sono presenti diversi `Dipartimenti` (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);

ogni `Dipartimento` offre più `Corsi di Laurea` (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni `Corso di Laurea` prevede diversi `Corsi` (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);

ogni `Corso` può essere tenuto da diversi `Insegnanti`;

ogni `Corso` prevede più `appelli` d'Esame;

ogni `Studente` è iscritto ad un solo `Corso` di Laurea;

ogni `Studente` può iscriversi a `più appelli` di Esame;

per `ogni appello d'Esame` a cui lo Studente ha partecipato, è necessario memorizzare il `voto` ottenuto, `anche se non sufficiente`. 

Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

## entiites
- Dipartimento
- corso di laurea
- corsi del corso (materie)
- insegnanti del corso
- appelli del corso
- studente
- voto

## tables
- dipartimenti
- corsi di laurea
- esami del corso
- insegnanti per materia
- studenti
- appelli
- voti


### dipartimenti
- id
- id_corsi
- nome del dipartimento

### corsi di laurea
- id 
- id_dipartimento
- nome_corso
- cfu_totali
- limite_partecipanti
- lingua
- tipo_laurea
- costo
- anno_accademico

### esami
- id
- id_insegnante
- id_corso_di_laurea
- lingua
- cfu_esame
- semestre
- anno_corso
- tipologia_esame
- modalità_valutazione

### insegnanti
- id
- id_esame
- nome
- cognome
- telefono
- indirizzo
- email

### studenti
- id
- id_corso_di_laurea
- nome
- cognome
- telefono
- indirizzo
- mail

### appelli
- id
- id_esame
- id_insegnante

### voti
- id
- id_studente
- id_insegnante
- esito
- votazione