# Journal M291

## Semaine 1 - 21.08.2026 P2-P4
- Création d'un repo sur github.com
- clonage dans VS Code
- Inscription à github education (pour certains)
- Inscrire l'url de son repo dans TEAMS

## Semaine 2 - 28.08.2026 P2-P4
- exercice e1-2b-page-profil.pdf (20min)
- Explication de la ligne 136 de mon code
- Mise en ligne avec GitHub Pages (Peut durer un certain temps (20min))


### Explication ligne 136
#### Explication des attributs `target` et `rel`

À la ligne 136, j'ai ajouté `target="_blank" rel="noopener noreferrer"` 
sur le lien GitHub.

##### `target="_blank"`

Ouvre le lien dans un **nouvel onglet** plutôt que de quitter la page. 
C'est utile pour un lien externe (GitHub) : le visiteur garde la page 
d'origine ouverte en même temps.

##### `rel="noopener noreferrer"`

C'est une mesure de sécurité, presque toujours utilisée avec 
`target="_blank"`. Elle contient deux mots-clés :

- **`noopener`** : empêche la nouvelle page (GitHub) d'accéder à la 
  page d'origine via JavaScript (par l'objet `window.opener`). 
  Sans cela, un site malveillant ouvert dans ce nouvel onglet pourrait 
  théoriquement manipuler la page d'origine (par exemple la rediriger 
  vers une fausse page). C'est ce qu'on appelle une faille de type 
  **"tabnabbing"**.

- **`noreferrer`** : empêche le navigateur d'envoyer l'information 
  "d'où vient le clic" (l'en-tête HTTP `Referer`) au site de 
  destination. Cela protège un peu la vie privée du visiteur. 
  Ce mot-clé inclut déjà le comportement de `noopener`, mais on 
  met souvent les deux ensemble par compatibilité avec les anciens 
  navigateurs.

#### En résumé

`rel="noopener noreferrer"` est une bonne pratique de sécurité à 
connaître dès qu'on utilise `target="_blank"`, même si rien ne 
"casse" techniquement si on l'oublie sur un site simple. C'est un 
bon réflexe à transmettre aux apprenants dès le début, pour qu'il 
devienne automatique.