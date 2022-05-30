# 🏗️: MOUNTAJRATE


Modélisation et implémentation de la base de données d’une application Web permettant d'exposer des produits locaux de la région
 - :date: Date Started: **26-05-2022.** 
 - :computer: Développé par: [LATIFA AMOUGUAY](https://github.com/LATIFADEV) && [ABDERRAHIM ELOUARDY](https://github.com/elouardyabderrahim)  && [ANAS MAKHLOUFI](https://github.com/anasmak04)
 - :office: Développé à: TechnoPark Agadir, Simplon Talent4Startups, Group *SoussTalents101*.
---

## Lien de l'espace de travail Trello
[Agile Sprint Board](https://trello.com/b/RCuXlj0C/montajrate)

## Énoncé de la portée du projet

<div style="display:flex">
<img src="/brief4-database/REPORT.PNG" height="200" width="300"/>

</div>

 [Cahier des charges du projet MOUNTAJARATE.](https://onedrive.live.com/edit.aspx?resid=EBEF1A2C83B13C3D!490&ithint=file%2cdocx)


## Diagramme de cas d'utilisation

<div style="display:flex">
<img src="/brief4-database/diagrame_cas_utilisation_1.png" height="200" width="300"/>
<img src="/brief4-database/diagrame_cas_utilisation2.png" height="200" width="300"/>
</div>

[cas_dutilisation_pharmacist.oom](/brief4-database/cas_dutilisation_pharmacist.oom)

## Diagramee de classe 

<div style="display:flex">
<img src="/brief4-database/diagrame_de_class.png" height="200" width="300"/>
</div>

[Diagramme_de_classes.moo](/brief4-database/Diagramme_de_classes.moo)
 ## USER STORY MAPPING
 
  [USER STORY MAPPING ](/brief4-database/USER_STORY_MAPPING.pdf)

## Migration de base de données 

  ```sql
  
  /*Create database:*/
  CREATE DATABASE "MOUNTAJRATE
  ---------------table of administrator----------
	create table Administrateur(id_administrateur serial primary key ,
    email VARCHAR(25),
    username  VARCHAR(25),
	passwrd VARCHAR(100)	 
	)
	-----------table of Client------------------

	create table Client(	id_client serial primary key   ,
    nom VARCHAR(25),
    prenom VARCHAR(100),
    email VARCHAR(25),
    date_naissance DATE,
    pays VARCHAR(10),
    ville VARCHAR(10),
    code_postal VARCHAR(5),
    username  VARCHAR(25),
	passwrd VARCHAR(100)	 
)
-----------------table of products---------------------
	create table Produit(id_produit serial primary key   ,
    nom_produit VARCHAR(25),
    type_produit VARCHAR(100),
    date_production DATE,
    qte_prod  int,
	prix_prd int,					 
    id_administrateur serial  REFERENCES Administrateur(id_administrateur) 
						)
	-----------------table of vote---------------------
	create table vote(
		id_produit serial references Produit(id_produit),
		id_client serial references Client(id_client),
		rate int
	)
	-------select table client ------------------
	 SELECT * FROM Client
	 --------select table administrator----------
	  SELECT * FROM Administrateur
	  ------------select table vote----------
	  SELECT * FROM vote
	  ------------select table vote----------
	  SELECT * FROM produit
	  -------------------------isertion du table CLient -------------
	 insert into Client(nom, prenom, email,date_naissance,pays,ville,code_postal,username,passwrd)values
	 ('amouguay', 'latifa', 'latifaamouguay@gmail.com','01-07-2000','MAROC','agadir',80650,'LATIFADEV','latifa123')
     insert into Client(nom, prenom, email,date_naissance,pays,ville,code_postal,username,passwrd)
     values('salma', 'alami', 'kawtaralami@gmail.com','01-01-2000','MAROC','agadir',80650,'salma','latifa123')
	 insert into Client(nom, prenom, email,date_naissance,pays,ville,code_postal,username,passwrd)
     values('rayan', 'hanae', 'kawtaralami@gmail.com','01-01-2000','MAROC','agadir',80650,'hanae','latifa123')
	 insert into Client(nom, prenom, email,date_naissance,pays,ville,code_postal,username,passwrd)
     values('fadli', 'KAWTAR', 'kawtaralami@gmail.com','01-01-2000','MAROC','agadir',80650,'fatima','latifa123')
	 insert into Client(nom, prenom, email,date_naissance,pays,ville,code_postal,username,passwrd)
     values('yahya', 'ilham', 'kawtaralami@gmail.com','01-01-2000','MAROC','agadir',80650,'ilham','latifa123')
	 insert into Client(nom, prenom, email,date_naissance,pays,ville,code_postal,username,passwrd)
     values('yahya', 'safia', 'kawtaralami@gmail.com','01-01-2000','MAROC','agadir',80450,'ilham','latifa123')
	 
	 ---------insertion les donées de l'administrateur------------------
	insert into Administrateur( email,username,passwrd)
     values( 'admin1@gmail.com','admin','admin')
	  
	 ---------insertion les donées du produit ------------------
	
	 --------- insertion des données des vote-------
	 ---------insertion les donées de l'administrateur------------------
	insert into vote( rate)
     values(4)
	 
	 
	 

	
  
```

## Outils

- PowerDesigner.
- MarkDown.
- Google Docs.
- PostgreSQL.
- Trello.
- Discord.

## Les 5W du projet

- **What?**   
 
   Réalisation d'une application web *SOUSS MONTAJRATE* permette d'exposer des produits locaux de région.
 
- **Why?** 

  Pour évaluer les produits de région .

- **Where?** 

  Les produits sont locaux au SOUSSMASSA/Maroc, mais ils sont destinés à être annoncés et votés à l'échelle internationale/mondiale.
  
- **When?**  

   chaque année

- **Who?**  

  les coopératifs de la région.
  

## Concepts Checklist

- [X] UML modeling.
- [X] Use case diagram.
- [X] class diagram.
- [X] PostgreSQL.
- [X] tables.
- [X] primary keys.
- [X] foreign keys.
- [X] SQL queries.
- [X] Agile method.
     - Deadline 2 days.
     - Team: Divide Tasks  Members Strenghts & Weakneses.
     - Validation: Versioning start with Important Features first
- [X] Scrum.
- [X] sprint.
- [X] Sprint backlog(To do list).
- [X] User Story Mapping.

