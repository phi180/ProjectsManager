# Progetto associato all'esame di SIW (AA 2019-2020)
##### Fippi Daniele, Celli Michael

Sono stati coperti tutti i casi d'uso con l'aggiunta delle estensioni (+ altre a piacere)

## Specifiche base

- Un Progetto ha un nome, una data di inizio e si compone di uno o più Task (attività)
- Ogni Progetto ha un proprietario (un utente del sistema) e può essere condiviso da uno o più utenti
- Ogni utente ha uno username e una password, un nome, un cognome, una data di creazione:
	- può essere proprietario di uno o più progetti e può avere visibilità su uno o più progetti (di cui non è proprietario)
	- si autentica sul sistema con un username (univoco) e password
	- può creare progetti
	- può aggiungere task ai propri progetti
	- può concedere la visibilità dei propri progetti ad altri utenti
- Ogni Task ha un nome, una descrizione, una data di creazione, ed è
assegnato ad un solo utente tra quelli che hanno visibilità sul
progetto

## Specifiche estese
- Ogni Progetto può essere associato ad uno o più Tag
- Ogni Task può essere associato ad uno o più Tag del progetto a cui appartiene, e ogni Tag può essere associato ad uno o più Task
- Ogni utente che abbia visibilità di un progetto può scrivere uno o più Commenti sotto qualsiasi Task di quel progetto

## Casi d'uso di presentazione (tutti + estensioni):

### User
- Signup
- Autenticazione
- Visualizzare il mio profilo
- Aggiornare il mio profilo (solo nome e cognome)

### Project
- Creare un nuovo progetto
- Visualizzare i miei progetti
- Visualizzare i progetti condivisi con me
- Aggiornare i dati di un mio progetto
- Cancellare un mio progetto
- Condividere un mio progetto con un altro utente
- Aggiungere un tag ad un mio progetto (estensione)
-- Eliminare membri dal progetto (estensione a piacere)

### Tag (estensione a piacere)
- Aggiornare i dati del tag
- Eliminare un tag dal progetto

### Task
- Aggiungere un nuovo Task a un mio progetto
- Aggiornare un Task di un mio progetto
-- Segnare un task come completato (estensione derivata dalla precedente)
- Cancellare un Task da un mio progetto
- Assegnare un Task di un mio progetto ad un utente che ha visibilità sul mio
progetto
- Aggiungere un Tag ad un task di un mio progetto (estensione)
- Aggiungere un Commento ad un Task di un progetto su cui ho visibilità
(estensione)

### Altro
- L'admin del sistema può visualizzare tutti gli utenti iscritti e cancellarli

## Altre note
- E' stato usato Bootstrap
- Implementato OAuth2 di Google. Funziona solo su localhost e modificando il file /etc/hosts (127.0.0.1 associato a me.mydomain.com). Le chiavi (riportate nel file properties) non sono state allegate in quanto private

