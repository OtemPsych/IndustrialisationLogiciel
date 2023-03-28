## Exercice 1: GitHub Actions

### Quelles étapes sont réalisées par cette action ?

- Installation des dépendances : `pip` et `flake8`.
- Lint

### Une étape est définie au minimum par 2 paramètres, lesquels sont-ils et à quoi servent-ils ?

- name : Le nom de l'étape.
- run : Le script contenant les commandes à exécuter.

### La première étape contient un paramètre ‘with’, a quoi sert-il ?

`with` définit comment le script est exécuté.

## Exercice 2: Qualité de code

### Sur l’onglet Summary d’une analyse de code, SonarCloud fournit 4 indicateurs. Quels sont-ils et quelles sont leurs utilités ?

- Bugs : Détails des bogues détectés.
- Code Smells : La dette technique et le taux d'endettement
- Vulnerabilities : Les vulnérabilités connues nécessitant une intervention immédiate
- Security Hotspots : Points sensibles en matière de sécurité

### À quoi sert l’indicateur Quality Gate ?
Une _quality gate_ est un indicateur qui nous permet de savoir si notre code répond au niveau minimum de qualité requis pour notre projet. Il s'agit d'un ensemble de conditions appliquées aux résultats de chaque analyse. Si les résultats de l'analyse remplissent ou dépassent les conditions de la porte de qualité, l'état est "Passé", sinon l'état est "Echec".