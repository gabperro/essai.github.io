# Étapes à suivre pour le projet

## 1. Préparer le projet
f
- Avoir un compte GitHub, Git et un éditeur de code. - Fait
- Créer un dépôt public à partir du modèle fourni. : Fait
- Nommer le dépôt `nomutilisateur.github.io`. : Fait 
- Cloner le dépôt sur son ordinateur et ouvrir le dossier du projet. : Fait 

## 2. Personnaliser le site
### Brainstorm 
Je veux un site web simple mais épuré. Je préfère blanc et noir, voire crème mais avec une police d'écriture style sérif, plus vieillot #*vintage*. 
### Étapes de modification : 
1. Remplacer le titre, le nom, la biographie et les autres renseignements personnels.
2. Je veux que la photo soit carrée.
3. Je veux changer les couleurs de la police et des sections pour aller du blanc au noir. 
4. Je veux une police d'écriture qui corresponde plus à mes attentes. 
5. Je veux pages (pas séparées):
   - Introduction avec liens vers les autres fichiers;  une courte biographie (Qui-je suis, ce que je fait, pourquoi?)
   - CV avec pdf fait avec Quarto, travaux marquants et recherche (plus tard, j'aimerais voir s'il serait possible de mettre les travaux quanti que j'ai fait sur R à Mannheim dans un repo github) 
   - Contacts. 
## 3. Publier les modifications

Après chaque série de changements, enregistrer le travail sur GitHub :

```bash
git add .
git commit -m "Mise à jour du site avec mes informations"
git push origin main
```

Il faut faire des commits régulièrement afin que le suivi du travail soit visible.

## 4. Activer GitHub Pages

- Dans le dépôt GitHub, ouvrir **Settings**, puis **Pages**.
- Choisir la branche **main** et le dossier **root** comme source.
- Enregistrer, puis vérifier le site à l'adresse `https://nomutilisateur.github.io`.

## 5. Vérifier les critères d'évaluation

- Le site est publié sur GitHub et le dépôt est accessible.
- Les commits montrent une progression régulière.
- Les sections essentielles sont complètes et le contenu est pertinent pour le cours.
- Le site est personnalisé au-delà des consignes de base, par exemple avec de nouvelles couleurs, un autre modèle ou des ajustements adaptés à ses besoins.

## Bonus facultatifs

- Relier le site à un nom de domaine personnalisé et activer HTTPS.
- Créer un CV en PDF avec Quarto, l'ajouter dans un dossier `cv`, l'intégrer au site et offrir un lien de téléchargement.




# Vagues de modifications
## Vague 1 : Style 
- Trouver polices d'écriture et les importer dans le main.css 
- Trouver des nouveaux icones plus neutres et stylés. 
- Créer des headers avec ces nouvelles polices. 
- Créer une nouvelle manière d'insérer photo (je veux carré). + à côté de l'introduction sur première page. 
- Changer les couleurs. 
## Vague 2 : Structure
- Effacer la grande image de fond. 
- Ajouter plusieurs sections en dessous de Introduction (qui-suis-je, que je fait, pourquoi?)
- Enlever section mes réalisations. 
- Ajouter CV avec Quarto + faire un page qui résume le CV avec le même style que la courrante page mes réalisations. 
- Ajouter lien vers courriel, facebook, linkedin et github dans Me joindre. 
## Vague 3: Contenu 
- Remplacer tous les *Votre nom* par Gabriel Perreault. 
- Remplacer *Le sous-titre de votre site* par *Introduction*. 
- Remplacer le Lorem Ipsum. 
- Remplacer les images. 
- Vérifier qu'aucun contenu n'est laissé. 

# Problèmes #
- Problème 2 : Les couleurs ne changent pas. 
  - Selon CODEX : d'autres règles que celle que j'avais modifier l'override. 
  - Solution : ligne 248, 2830, 2874, 2923, 2931
Probleme 5 : Tous les icones et boutons sont de la bonne couleur, sauf email, qui reste noir dans les brand icons. 
- Premier fixe : changer couleur de .solid 
Probleme 6 : je sais pas ce que j'ai fait mais j'ai tout brisé avec mon dernier move qui était d'ajouter science politique à mon header. 
- Premier fix : Revenir en arrière 
- Deuxieme fix : diagnostic par Codex.Le probleme venait de mon changement icone email. f
- Troisieme fix : Site web toujours brise. Deuxieme diagnostic plus large et restauration par codex. 
Probleme 8 : La photo avatar est restee ronde. 
Probleme 9 : texte italique reste le meme. 
FIX 1 : Trouver P BR dans main.css
