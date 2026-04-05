# Questionnaire Kobo – Ménage détaillé et groupes spécifiques

Ce projet contient un formulaire **XLSForm** orienté secteur du développement, conçu pour démontrer une collecte de données ménage plus riche et plus réaliste.

## Contenu
- `forms/kobo_xlsform_menage_detaille_style.xlsx` : formulaire principal
- `README.md` : description du projet

## Principales améliorations
- Roster détaillé des membres du ménage
- Variables individuelles pour chaque membre :
  - prénom
  - nom
  - sexe
  - date de naissance
  - âge calculé automatiquement
  - lien avec le chef de ménage
  - niveau d’instruction
  - statut d’activité
  - statut matrimonial
- Modules conditionnels dédiés à des groupes spécifiques :
  - **enfants**
  - **femmes et filles**
  - **retraités et personnes âgées**
- Rubriques ménage consolidées sur :
  - les enfants
  - les femmes
  - les personnes âgées
- Calculs automatiques :
  - âge à partir de la date de naissance
  - ratio de dépendance
  - solde mensuel du ménage

## Logique du formulaire
Le formulaire est structuré en plusieurs rubriques :
1. Identification et métadonnées
2. Profil du ménage
3. Roster détaillé des membres
4. Rubrique ménage – Enfants
5. Rubrique ménage – Femmes
6. Rubrique ménage – Retraités et personnes âgées
7. Moyens d’existence et revenus
8. Accès aux services sociaux de base
9. Habitat, biens et preuves

## Exemple de calcul d’âge
Le champ âge est calculé automatiquement à partir de la date de naissance :

```text
int((today() - ${member_dob}) div 365.25)
```

## Utilisation dans KoboToolbox
1. Ouvrir KoboToolbox
2. Créer un nouveau projet
3. Importer le fichier XLSForm
4. Vérifier le déploiement
5. Tester le formulaire dans l’aperçu

## Remarque
Le fichier a été stylisé pour ressembler à un classeur XLSForm professionnel :
- en-têtes turquoise foncé
- sections visuellement distinguées
- lignes de calcul, note, groupe et repeat colorées
