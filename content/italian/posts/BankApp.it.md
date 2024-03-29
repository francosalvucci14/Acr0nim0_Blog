---
title: "Bank App"
date: 2023-03-10T14:44:44+01:00
draft: false
featuredImage: "/images/BankApp/BankLogo.jpg"
featuredImagePreview: "/images/BankApp/BankLogo.jpg"
lightgallery: true
tags:
    - "Project"
    - "Bank App"
    - "Java"
    - "MySql"
toc:
  enable: true
  auto: true
share:
  enable: true
comment:
  enable: true
---

# Idea
L'idea mi è venuta totalmente random, mentre non facevo un bel niente :joy:

Ho visto qualche video su youtube e mi sono deciso di approcciarmi a questa "challenge" (mettiamola tra virgolette perchè poi si vedrà che non è una vera e propria challenge)

L'idea che sta alla base è molto semplice, un'interfaccia (chiamiamola HOME) dove ci sono i collegamenti alle altre interfacce : Prelievo, Deposito, Show Utenti e cos' via...

# Servizi
I servizi offerti da questa app sono :
- Prelievo dei soldi dal conto
- Deposito soldi sul conto
- Show degli utenti
- Ricerca conto tramite nome account
- Cambio numero account tramite nome utente

# Realizzazione
L'app è stata realizzata tramite il linguaggio Java, e utilizza un database MySql per lo storage e modifica dei dati
L'ide utilizzato è Ecplise
Tutte le interfaccie sono state realizzate tramite Java AWT, quindi il codice risulterà poco chiaro (allego immagini delle interfacce)
# Codice

Il codice di questa applicazione lo trovate tutto sul mio GitHub
Link qui --> [Bank App](https://github.com/francosalvucci14/Bank-App)

Queste sono gli screenshots delle varie interfacce<br/>
Home Page:<br/>
{{< figure src="/images/BankApp/Home.png" title="Home page" alt="Home">}}<br/>
Cambio Dettagli Account:<br/>
{{< figure src="/images/BankApp/ChangeAccountDet.png" title="Cambia Dettagli Account" >}}<br/>
Prelievo:<br/>
{{< figure src="/images/BankApp/Prelievo.png" title="Prelievo" >}}<br/>
Registra Utente:<br/>
{{< figure src="/images/BankApp/RegisterUser.png" title="Registra Utenti" >}}<br/>
Show degli utenti:<br/>
{{< figure src="/images/BankApp/ShowUser.png" title="Ricerca Utenti" >}}<br/>

# Database
Il database è stato realizzato su DBMS **MySql**, ed è organizzato in questo modo:

- Ci sono due tabelle, "Utenti" e "Credito"
	- Nella tabella Utenti ci sono i seguenti campi:
		- UID -> User ID (**chiave primaria**)
		- User -> Nome utente
		- Pass -> Password
		- NConto -> Numero del conto corrente
	- Nella tabella Credito ci sono i seguenti campi:
		- CID -> Conto ID (**chiave primaria**)
		- UserID -> User ID (chiave secondaria relativa alla chaive UID della tabella Utenti)
		- Credito -> Credito del conto

Ogni volta che un'utente viene inserito nello schema, gli viene dato un numero di conto in modo random, con credito 0, e nel DB viene collegato alla tabella Credito
Le tabelle sono collegate da una relazione **1:1**
{{< typeit code=java >}}
public class Thanks{
  public static void main(String[] args){
    System.out.println("Grazie per aver letto :smile:");
  }
}
{{< /typeit >}}

