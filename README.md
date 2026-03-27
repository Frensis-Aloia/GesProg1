# GesProg1

# Documentazione del Sistema Informativo

> Documentazione Tecnica
> Versione: 1.0.0
> Stato: Bozza
> Ultimo aggiornamento: 2026-03-27
> Autore/i : Frensis 

# 1. Abstract

Il software permette all'utente di salvare una lista json contenente password, email e nome del servizio; l'utente interisce una chiave mastre per decriptare tutte le credenziali e la reinserisce per decriptarle.
---

# 2. Introduzione

 Praticamente l'idea del progetto mi è venuta dal fatto che oggigiorno facciamo, volenti o nolenti, un sacco di collegamenti ad account online per il cui non si può usare la stessa password per
   due motivi: perché sarebbe non sicuro e perché ogni sito ha un requisito diverso (carattere speciale, caratteri numeri, numero di caratteri, non contenga password "facili"...).
   Allora sorge il problema di ricordarle tutte, email comprese (per chi ha più email), allora avevo pensato a questo software.
   I dati sono salvati in un file json in un oggetto con 3 variabili, il nome del servizio, l'email/username dell'account e la password; il programma funziona che quando si mette una password che serve
   da "chiave maestra" nel form il programma, succede che vengono criptati tutti i dati contenuti nel json.
   Se voglio leggere i dati basta mettere nuovamente la CM, che diventa l'unica password da ricordare da questo momento in poi, e i dati verranno decriptati.
--

# 3. Panoramica del Sistema

Il gestore password è un programma basato su C# dove i dati vengono salvati in locale con un file json, essendo un programma locale non fa uso di server o api.

---

## 3.2 Stack Tecnologico

| Livello | Tecnologia |
|----------|-----------|
| Frontend | C#|
| Backend | C#|
| Database | Json|
| Autenticazione | n/d|
| Infrastruttura | C#|

---

# 4. Data Flow Diagram (DFD)

Non ci sono entità esterne, il processo principale del sistema è quello che legge o modifica il file json.

| ID Processo | Nome Processo | Descrizione |
|------------|--------------|------------|
| P1 | Cripta/Decripta| Dopo aver ricevuto la chiave la usa per criptare/decriptare i dati|
| P2 | Inserisci| Inserisce delle nuove credenziali nel database|

---

# 5. Requisiti di Sistema

| ID | Descrizione del Requisito | Priorità |
|----|--------------------------|----------|
| RF-01 | Il sistema deve criptare/decriptare i dati con la chiave maestra. Alta priorità | Alta |
| RF-02 | Il sistema deve permettere l'inserimento di nuovi account. Alta priorità | Media |

---

## 5.2 Requisiti Non Funzionali

I requisiti non funzionali definiscono attributi di qualità.

### Prestazioni
- Tempo massimo di risposta: 3s 
- Numero di utenti concorrenti supportati: 1
- Throughput: 3Mbps

### Sicurezza
- Metodo di autenticazione:  n/d
- Modello di autorizzazione:  n/d
- Crittografia dei dati:  algoritmo F.d.F
- Logging e audit:  n/d

### Affidabilità
- Strategia di backup:  n/d
- RTO (Recovery Time Objective): n/d  
- RPO (Recovery Point Objective):  n/d

### Scalabilità
- Scalabilità orizzontale:  n/d
- Scalabilità verticale:  n/d

### Usabilità
- Conformità accessibilità: n/d  
- Browser supportati:  n/d
- Responsive design:  n/d

---

## 5.3 Requisiti Hardware

| Componente | Requisito Minimo |
|------------|-----------------|
| CPU | 1GhZ |
| RAM | 1gb |
| Storage | 10MB |

---

## 5.4 Requisiti Software

| Componente | Versione |
|------------|---------|
| Sistema Operativo |Windows 10/11|
| Database |Json|
| Runtime |n/d|
| Browser |n/d|

---

## 6) non pervenuto

   (marco marco...)

