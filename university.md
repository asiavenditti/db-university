Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:

- sono presenti diversi `Dipartimenti` (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni `Dipartimento` offre più `Corsi di Laurea` (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni `Corso di Laurea` prevede diversi `Corsi` (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni `Corso` può essere tenuto da diversi `Insegnanti;
- ogni `Corso` prevede più appelli d'`Esame`;
- ogni `Studente` è iscritto ad un solo `Corso di Laurea`;
- ogni `Studente` può iscriversi a più appelli di `Esame`;
- per ogni appello d'`Esame` a cui lo `Studente` ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente. Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

# entità

- Dipartimenti
- Corsi di Laurea
- Corsi 
- Insegnanti
- Studenti
- Esami
- Dettagli esame


## dipartimenti

- id PRIMARY KEY
- name
- email
- phone
- address

## corso_di_laurea

- id PRIMARY KEY
- dipartimento_id 
- subject

## corsi

- id PRIMARY KEY
- corso di laurea_id
- name

## insegnanti

- id PRIMARY KEY
- name
- lastname
- email
- phone


## corsi_insegnanti (tabella ponte)
- insegnante_id
- corso_id


## studenti

- id PRIMARY KEY
- corso_di_laurea_id
- name
- lastname
- email

## esami
- id PRIMARY KEY
- studente_id
- corso_id
- data


## dettagli_esame
- id PRIMARY KEY
- voto
- esito

