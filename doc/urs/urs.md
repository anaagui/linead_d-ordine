### LIBRERY-BOOK 
##### DIBRIS – Università di Genova. Scuola Politecnica, Software Engineering Course 80154


**VERSION : 1.0**

**Authors**  
ANA
AGUILAR

**REVISION HISTORY**

| Version    | Date        | Authors      | Notes        |
| ----------- | ----------- | ----------- | ----------- |
|1.0 |25/06/2024  |Ana Aguilat | Inserita prima immagine |
|2.0 |25/06/2024  |Ana Aguilar | Inserita Book 	         |
|3.0 |25/06/2024  |Ana Aguilar | Inseriti Scenari	 |	
# Table of Contents

1. [Introduction](#p1)
	1. [Document Scope](#sp1.1)
	2. [Definitios and Acronym](#sp1.2) 
	3. [References](#sp1.3)
2. [System Description](#p2)
	1. [Context and Motivation](#sp2.1)
	2. [Project Objectives](#sp2.2)

  

<a name="p1"></a>

## 1. Introduction

<a name="sp1.1"></a>

### 1.1 Document Scope


<a name="sp1.2"></a>

### 1.2 Definitios and Acronym


| Acronym				| Definition | 
| ------------------------------------- | ----------- | 
| XXXX                                  | XXXX |

<a name="sp1.3"></a>

### 1.3 References 

<a name="p2"></a>

## 2. System Description
<a name="sp2.15"></a>

Si progetti un software nel quale l'Utente gestiore un DataBase di una Libreria, dove l'Utente interagisce con il software il quale permette l'ingresso al DataBase tramite tastiera per l'input e output dei dati corrispondenti ai LIBRI, come l'ISBN, titolo del libro, autore e anno di edizione che dovrebbero apparire sullo schermo





### 2.1 Context and Motivation

<a name="sp2.2"></a>

### 2.2 Project Obectives 

<a name="p3"></a>


## 3. Requirements

| Priorità | Significato | 
| --------------- | ----------- | 
| M | **Mandatory:**   |
| D | **Desiderable:** |
| O | **Optional:**    |
| E | **future Enhancement:** |

<a name="sp3.1"></a>
### 3.1 Stakeholders
Utente : L'Utente è un operatore che gestisce il programma BookLibrary nel quale può Visualizare i libri esistenti, Aggiungere nuovi libri, Rimuovere libri, Cercare libri, Caricare sul file CSV, Salvare sul file CSV, Ordinare sul file CSV, e uscire dal programma.

![Use case banca](imgs/Book.png)


<a name="p3"></a>
#### 3.2.1 Visualizza Libro
<b>Nome</b> VisualizzaLibro

<b>Precondizioni</b>

<b>Priorità</b>

<b>Stakeholder Principale</b> Utente

<b>Scenario Principale</b>

1. Utente chiede al sistema di visualizare i suoi libri

2. il Sistema mostra i libri

3. il Sistema saluta


<b>Scenario Alternativo</b>   

2A - Non ci sono libri salvati

	1. il sistema notifica l'utente che il DataBase è vuoto
	

<a name="p3"></a>
#### 3.2.2 Aggiungere Libro

<b>Nome</b> AggiungereLibro

<b>Precondizioni</b>

<b>Priorità</b>

<b>Stakeholder Principale</b> Utente

<b>Scenario Principale</b>

1. il sistema chiede d'inserire il titolo
2. l'utente inserisce un titolo
3. il sistema chiede d'inserire nome autore
4. l'utente inserisce nome autore
5. il sistema chiede d'inserire anno
6. l'utente inserisce anno
7. il sistema chiede d'inserire ISBN
8. l'utente inserisce l'ISBN
9. il sistema valida l'inserimento
10. il sistema inserisce il libro nel DataBase
11. il sistema saluta e chiude
 
<b>Scenario Alternativo</b>

2A - L'utente inserisce un titolo invalido

	1. il sistema notifica titolo invalido
	2. il sistema torna al punto 1 dello scenario principale
	   
9A - Esiste già un libro con lo stesso ISBN

	1. il sistema avvisa l'utente della esistenza del libro
	2. il sistema mostra il libro con lo stesso ISBN
	3. il sistema chiede se vuole sostituire il libro
	4. l'utente dice di si
	5. il sistema cancella il vecchio libro
	6. l'utente inserisce il nuovo libro
	7. il sistema torna al punto 11 dello scenario principale

9A 4A - Utente dice di no

	1. il sistema chiede se si vuole modificare l'ISBN
	2. utente dice di si
	3. il sistema torna al punto 8 dello scenario principale

9A 4A 2A - Utente scrive nuovo ISBN

	1. il sistema notica che il libro è giusto
	2. il sistema torna al punto 11 dello scenario principale
   
   
<a name="p3"></a>
#### 3.2.3 Rimuovere Libro

<b>Nome</b> RimuovereLibro

<b>Precondizioni</b>

<b>Priorità</b>

<b>Stakeholder Principale</b> Utente

<b>Scenario Principale</b>

1. Utente chiede al sistema di rimuovere un libro
2. il sistema chiede di inserire ISBN del libro da rimuovere
3. l'utente inserisce l'ISBN
4. il sistema mostra il libro da rimuovere e chiede se si vuole rimuovere
6. l'utente dicie di si
7. il sistema rimuove il libro
8. il sistema chiede se si vuole rimuovere un altro libro
9. l'utente dice di si
10. si torna al punto 2
11. il Sistema saluta e chiude

<b>Scenario Alternativo</b> 

3A - Se l'utente inserice un ISBN inesistente

	1. il sistema notifica che non sono presenti libri con lo stesso ISBN
	2. il sistema torna al punto 2 dello scenario principale
 
6A - Se l'utente dice di no

 	1. il sistema torna al punto 8 dello scenario principale

9A - Se l'utente dice che non vuole rimuovere altro libro

	1. il sistema torna al punto 11 dello scenario principale
	

<a name="p3"></a>
#### 3.2.4 Cercare LIbro

<b>Nome</b> CercaLibro

<b>Precondizioni</b>

<b>Priorità</b>

<b>Stakeholder Principale</b> Utente

<b>Scenario Principale</b>

1. l'utente chiede di cercare libro
2. il sistema chiede di inserire l'ISBN
3. l'utente inserisce ISBN
4. il sistema valida l'inserimento
5. il sistema mostra il libro
6. il sistema saluta e chiude

<b>Scenario Alternativo</b>
2A - L'utente inserisce un ISBN invalido

	1. il sistema notifica ISBN non trovato
	2. il sistema torna al punto 2 dello scenario principale
	   
<a name="p3"></a>
#### 3.2.5 Caricare Libro su fie CSV

 <b>Nome</b> CaricaLibroCSV

<b>Precondizioni</b>

<b>Priorità</b>

<b>Stakeholder Principale</b> Utente

<b>Scenario Principale</b>

1. L'utente chiede di caricare un libro sul file CSV
2. Se il file CSV esiste il sistema notifica la presenza del file
3. il sistema chiede d'inserire dell'ISBN
4. l'utente inserisce l'ISBN
5. il sistema chiede d'inserire il titolo
6. l'utente inserisce un titolo
7. il sistema chiede d'inserire nome autore
8. l'utente inserisce nome autore
9. il sistema chiede d'inserire anno
10. l'utente inserisce anno
11. il sistema notifica che il libro è stato caricato sul file CSV
12. il sistema chiede se si vuole caricare altri libri sul file CSV
13. il cliente dice di Si
14. il sistema torna al punto 2
15. il sistema saluta e chiude
 
<b>Scenario Alternativo</b>

2A - Se il file CSV non esiste

	1. il sistema notifica File non trovato
	2. il sistema torna al punto 15 dello scenario principale

 11A - se il sistema non ha caricato il file

  	1. il sistema notifica che il file non è stato caricato correttamente
   	2. il sistema torna al punto 12 dello scenario principale

 13A - il cliente dice no

 	1. il sistema torna al punto 15 dello scenario principale
	   

<a name="p3"></a>
#### 3.2.6 Salvare LIbro

 <b>Nome</b> SalvaLibro

<b>Precondizioni</b>

<b>Priorità</b>

<b>Stakeholder Principale</b> Utente

<b>Scenario Principale</b>
  


<a name="p3"></a>
#### 3.2.7 Ordinare LIbro

 <b>Nome</b> OrdinaLibro

<b>Precondizioni</b>

<b>Priorità</b>

<b>Stakeholder Principale</b> Utente

<b>Scenario Principale</b>
  
1. l'utente chiede di ordinare i libri presenti sul file CSV
2. il sistema mostra la sceltra tra ISBN, Titolo, Autore e Anno
3. l'utente sceglie l'ordinamento per ISBN
4. il sistema chiede si inserire ISBN
5. l'utente inserisce ISBN
6. il sistema mostra i libri ordinati per ISBN in modo ascendente 
7. il sistema mostra elenco file ordinato in modo ascendente
8. il sistema chiede
9.  l'utente sceglie l'ordinamento per ISBN
4. il sistema chiede si inserire ISBN
5. l'utente inserisce ISBN
6. il sistema mostra i libri ordinati per ISBN in modo ascendente 
7. il sistema mostra elenco file ordinato in modo ascendente
