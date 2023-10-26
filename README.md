# Entête
   
    Projet: 	Laboratoire: Application comptes utilisateurs (Android Studio en java)
    Codeurs:	Mathieu Hatin (2296939)
    Cours: 		Applications natives sous android 1 (420-325-AH)
	Date:		Octobre 2023

## Installation nécessaire

    Le projet se trouve sur github à l'adresse
    https://github.com/hatmath/UsersAccountsApp

    Voir le fichier README-GITHUB-IMPORTATION.MD si vous avez besoin d'aide

    Les test pour cette application on été fait avec un emulateur Pixel 3a API 24.
    Pourquoi pas la dernière version de l'API?
        Pour que la fonctionnalité mailto: fonctionne bien sinon avec l'API 34 tout fonctionnera 
        sauf l'envoie de courriel

## Énoncé

	Sous Android Studio, en java, écrit moi une application qui doit permettre à l’utilisateur de se connecter.
	Il faut valider que les informations saisies sont correctes sinon l’accès sera refusé.
	Nous avons deux types d’utilisateurs :
	Les administrateurs qui ont pour rôles :
	 - Consulter la liste des utilisateurs inscrits (Afficher uniquement les noms et prénoms)
	 - Ajouter un utilisateur
	 - Supprimer un utilisateur
	 - Consulter les informations d’un utilisateur
	 - Envoyer un courriel à un utilisateur
	 
	Les utilisateurs ont pour rôles :
	 - S’enregistrer pour la première connexion
	 - Modifier ses données
	 - Envoyer un courriel aux administrateurs

	Les informations des utilisateurs devront contenir :
	 - Nom et prénoms
	 - Date de naissance
	 - Adresse (numéro, rue, ville, province, code postal et pays)
	 - Profession
	 - Adresse électronique (valide)
	 
## Clarifications

	Clarification de la logique de l'application

	* utilisateur veux dire utilisateur ordinaire
	** admin est un utilisateur de type administrateur
	*** super fait référence au super utilisateur 
	
	- Les utilisateurs et les admin s'inscrive via l'interface de connexion/inscription
	- Le super déterminer qu'un utilisateur est un admin ou non ultérieurement
	- Les utilisateurs et les admin peuvent aussi être créé par le super via son interface d'adminitration plus permissive
	- Idéalement, il serait bien qu'un utilisateur/admin recoivent un email de validation afin de valider son compte. Mais pour l'instant, nous allons simplement donner la permission à n'importe quel admin de valider les nouveaux comptes utlisateurs. Seul le super peut valider les admin. Et bien sûr, il peut valider les utilisateurs aussi.
	- Sans cette validation, l'utilisateur qui viens de s'inscrire ne peux se connecter.
	- À chaque jour, à une heure définie, les comptes non validé pourraient être supprimés (en théorie)
	- Le super voit tout le monde. Les admin voit les utilisateurs. Les utilisateurs ne voit qu'eux-même.
	- La logique pour l'envoie de courriels:
		- Le super peux envoyer des courriels à tous le monde individuellement
		- Les admin peuvent envoyer des courriels à tous le utilisateur individuellement
		- Les utilisateurs peux envoyer un courriel à une adresse de support 		
	- Pour l'instant n'importe qui peux modifier les informations le concernant et ceux des utilisateurs qu'il voit.  
	- Ultériueurement, il faudrait détenir le PIN qui lui est encrypté et connu de l'utilisateur seulement pour modifier les données sensibles le concernant. Le code est partiellemeent en place

## À faire / Correction / Amélioration
