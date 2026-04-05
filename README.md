# Questionnaire Kobo / XLSForm — secteur du développement

## Contenu
- `kobo_xlsform_tous_types.xlsx` : le formulaire principal au format XLSForm.
- `villages.csv` : liste externe utilisée par la question `select_one_from_file`.
- `support_services.csv` : liste externe utilisée par la question `select_multiple_from_file`.

## Thème
Enquête sur les conditions de vie, l’accès aux services de base et l’inclusion socio-économique des ménages.

## Ce que le formulaire couvre
Ce modèle explore les principaux types Kobo/XLSForm suivants :
- `acknowledge`
- `text`
- `integer`
- `decimal`
- `range`
- `select_one`
- `select_multiple`
- `rank`
- `date`
- `time`
- `datetime`
- `geopoint`
- `geotrace`
- `geoshape`
- `image`
- `audio`
- `video`
- `file`
- `barcode`
- `calculate`
- `hidden`
- `select_one_from_file`
- `select_multiple_from_file`
- `note`

## Feuilles du XLSForm
### 1) survey
Contient les questions, la logique, les contraintes, les calculs et les apparences.

### 2) choices
Contient les listes de choix internes (`sex`, `yes_no`, `quality`, etc.).

### 3) settings
Contient les paramètres du formulaire :
- `form_title`
- `form_id`
- `version`
- `default_language`
- `style`

Le fichier utilise le style `theme-grid no-text-transform` pour mieux simuler une section « tableau de questions » dans Enketo.

## Important : question matrix / tableau de questions
Dans KoboToolbox, la question matrix est une fonctionnalité du Formbuilder/Enketo Grid. Elle n’est pas un type XLSForm natif distinct. Quand elle est représentée en XLSForm, elle devient une structure de groupe avec des `w-values` (par exemple `w4`, `w2`).  
Dans ce modèle, la section **Accès aux services** joue ce rôle.

## Important : fichiers externes
Les questions suivantes ont besoin de fichiers externes :
- `select_one_from_file villages.csv`
- `select_multiple_from_file support_services.csv`

### Après import du XLSForm dans KoboToolbox
1. Ouvre le projet.
2. Va dans **Paramètres > Médias**.
3. Téléverse `villages.csv`.
4. Téléverse `support_services.csv`.
5. Redéploie le formulaire si nécessaire.

## Conseils d’utilisation
- Utilise ce fichier comme base de portfolio ou comme bac à sable pour apprendre Kobo.
- Teste le rendu à la fois dans **Enketo** et dans **KoboCollect**, car certaines apparences diffèrent selon la plateforme.
- Les questions de type code-barres / QR code sont surtout utiles dans KoboCollect sur mobile.

## Références KoboToolbox
- Question types in XLSForm: https://support.kobotoolbox.org/question_types_xls.html
- Question appearances in XLSForm: https://support.kobotoolbox.org/appearances_xls.html
- Question options in XLSForm: https://support.kobotoolbox.org/question_options_xls.html
- Selecting options from an external file in XLSForm: https://support.kobotoolbox.org/select_from_file_xls.html
- Creating a question matrix in the Formbuilder: https://support.kobotoolbox.org/matrix_response.html
- Styling your forms using XLSForm: https://support.kobotoolbox.org/form_style_xls.html
