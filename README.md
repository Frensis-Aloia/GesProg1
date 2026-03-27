# GesProg1

Documentazione Tecnica
Versione: 1.0.0
Stato: Bozza
Ultimo aggiornamento: 2026-03-27
Autore/i : Frensis

1) Il software permette all'utente di salvare una lista json contenente password, email e nome del servizio; l'utente interisce una chiave mastre per decriptare tutte le credenziali e la reinserisce per decriptarle.

2) Praticamente l'idea del progetto mi è venuta dal fatto che oggigiorno facciamo, volenti o nolenti, un sacco di collegamenti ad account online per il cui non si può usare la stessa password per
   due motivi: perché sarebbe non sicuro e perché ogni sito ha un requisito diverso (carattere speciale, caratteri numeri, numero di caratteri, non contenga password "facili"...).
   Allora sorge il problema di ricordarle tutte, email comprese (per chi ha più email), allora avevo pensato a questo software.
   I dati sono salvati in un file json in un oggetto con 3 variabili, il nome del servizio, l'email/username dell'account e la password; il programma funziona che quando si mette una password che serve
   da "chiave maestra" nel form il programma, succede che vengono criptati tutti i dati contenuti nel json.
   Se voglio leggere i dati basta mettere nuovamente la CM, che diventa l'unica password da ricordare da questo momento in poi, e i dati verranno decriptati.

3) Il gestore password è un programma basato su C# dove i dati vengono salvati in locale, essendo un programma locale non fa uso di server o api.

4) Non ci sono entità esterne, il processo principale del sistema è quello che legge o modifica il file json.

5) RF-01: Il sistema deve criptare/decriptare i dati con la chiave maestra. Alta priorità
   RF-02: Il sistema deve permettere l'inserimento di nuovi account. Alta priorità

6) non pervenuto
     
