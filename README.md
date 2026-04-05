# Questionnaire Kobo – Ménage 

Ce projet contient un formulaire **XLSForm** orienté secteur du développement, conçu pour démontrer une collecte de données ménage plus riche et plus réaliste en utilisant plusieurs types de variables.

## Fichiers du projet

```text
kobo_github_project/
├── forms/
│   └── kobo_xlsform_menage.xlsx
├── external_choices/
│   ├── villages.csv
│   └── support_services.csv
└── README.md
```
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

## Import dans KoboToolbox


1. Ouvre KoboToolbox.
2. Crée un nouveau projet à partir d’un fichier XLSForm.
3. Importe `forms/kobo_xlsform_menage.xlsx`.
4. Si Kobo demande les listes externes, ajoute aussi :
   - `external_choices/villages.csv`
   - `external_choices/support_services.csv`

## Auteur
Patricia KOTO

