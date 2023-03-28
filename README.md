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

### Quelle est la différence entre les sections New code et Overall Code dans l’onglet Summary ?

- New Code : 0 bugs, 0 code smells, 0 vulnerabilities, 0 security hotspots, 50.0% coverage, 0.0% duplications
- Overall Code : 0 bugs, 3 code smells, 0 vulnerabilities, 1 security hotspots, 76.5% coverage, 0.0% duplications

Le dernier commit n'a pas ajouté de nouveau code, c'est donc normal que les indicateurs de New Code soient tous à 0.

### Y a-t-il des Code Smells ? Si oui, combien et pour quelle(s) raisons(s) ?

Il y en a trois :

- 'Remove unused function parameter "deferred"' de la méthode `spend_cash`.
- Les méthodes `spend_cash` et `spend_money` sont identiques.

### Y a-t-il des Security Hotspots ? Si oui, combien et pour quelle(s) raison(s) ?

- L'image python est exécutée avec root.