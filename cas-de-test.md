# Catalogue des Cas de Test

| ID | Module | Description | Données d'entrée | Résultat attendu |
|----|--------|-------------|------------------|------------------|
| TC-01 | Authentification | Connexion valide | Identifiant: "etudiant", Mot de passe: correct | Redirection vers la page d'accueil |
| TC-02 | Authentification | Connexion mauvais mot de passe | Identifiant: "etudiant", Mot de passe: "faux" | Message d'erreur, pas de connexion |
| TC-03 | Authentification | Connexion identifiant vide | Identifiant: "", Mot de passe: "123" | Message d'erreur, pas de connexion |
| TC-04 | Authentification | Déconnexion | Clic sur le bouton "Déconnexion" | Retour à la page de login |
| TC-05 | Création Rapport | Création valide | ID: "R002", Titre: "Rapport de stage" | Le rapport apparaît dans la liste |
| TC-06 | Création Rapport | Titre vide | ID: "R003", Titre: "" | Message d'erreur (Refus de création) |
| TC-07 | Création Rapport | Titre trop court (2 car.) | ID: "R004", Titre: "ab" | Message d'erreur (Refus de création) |
| TC-08 | Création Rapport | Titre trop long (150 car.) | ID: "R005", Titre: "aaaa...150" | Message d'erreur (Refus de création) |
| TC-09 | Création Rapport | ID en doublon | ID: "R001" (existant), Titre: "Test" | Message d'erreur (Refus de création) |
| TC-10 | Liste | Affichage de la liste | Clic sur "Voir la liste" | Tableau avec les rapports affichés |
| TC-11 | Liste | Statut initial | Création d'un nouveau rapport | Le statut est "Soumis" |
| TC-12 | Persistance | Rechargement de la page | F5 sur la liste des rapports | Les rapports sont toujours là |
| TC-13 | Sécurité | Accès direct sans login | URL: localhost:8080/creer.html | Redirection vers login |
| TC-14 | Sécurité | Accès direct à la liste sans login | URL: localhost:8080/liste.html | Redirection vers login |
| TC-15 | API (Postman) | Requête POST création sans token | Envoi d'une requête POST sans être connecté | Code HTTP 401 ou 403 (Non autorisé) |