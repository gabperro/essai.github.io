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
Avant : régler le problème avec l'index actuel : le side pannel ne fonctionne pas sur le site Web. Il apparaît juste quand le site n'est pas en plein écran. 
1. Remplacer le titre, le nom, la biographie et les autres renseignements personnels.
2. Je veux que la photo soit carrée dans le side pannel. 
3. Je veux changer les couleurs de la police et des sections pour aller du blanc au noir. 
4. Je veux une police d'écriture qui corresponde plus à mes attentes. 
5. Je ne veux pas de grosse photo d'arrière plan. Mais plutôt une bannière avec des liens vers les pages à droite et mon nom Gabriel Perreault - Science politique à gauche.  
6. Je veux pages (pas séparées): 
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
- Insérer boutons à mettre sur bannière. 
- Ajouter des lignes blanches entre les sections dans side panel. 
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
- Problème 1 : le side pannel demeure ouvert tout le temps si en plein écran. 
 - Après premiers changement : fonctionne pas. 
 - Selon CODEX : je m'adressais pas à la bonne section 
  - Solution : #main.css(line2800) - fixer côté droit
  - La solution n'a pas fonctionné. On va restaurer le code comme il l'était dans le template. 
- Problème 2 : Les couleurs ne changent pas. 
  - Selon CODEX : d'autres règles que celle que j'avais modifier l'override. 
  - Solution : ligne 248, 2830, 2874, 2923, 2931
Problème 3 : Les couleurs du side pannel n'ont pas changé. 
- Selon CODEX : j'ai somehow pas push (oups)
- Fixed
Probleme 4 : Je veux que la banniere reste tout le temps ouverte : 
- Premier fix : nouvelle regle. 
- Deuxieme fix : s'inspirer du header d'une autre template
- Troisieme fix : abandonner 
Probleme 5 : Tous les icones et boutons sont de la bonne couleur, sauf email, qui reste noir dans les brand icons. 
- Premier fixe : changer couleur de .solid 
Probleme 6 : je sais pas ce que j'ai fait mais j'ai tout brisé avec mon dernier move qui était d'ajouter science politique à mon header. 
- Premier fix : Revenir en arrière 
- Deuxieme fix : diagnostic par Codex.Le probleme venait de mon changement icone email. f
- Troisieme fix : Site web toujours brise. Deuxieme diagnostic plus large et restauration par codex. 
Probleme 7 : Le bouton du side pannel est encore vieille couleur. 
- Fix : Trouver avec Codex : ligne 3213. Changer couleur 
Probleme 8 : La photo avatar est restee ronde. 
Probleme 9 : texte italique reste le meme. 
FIX 1 : Trouver P BR dans main.css
Probleme 10 : Avec nouvelle regle : image couvre top. 
Fix 1: Trouver #header et ajouter z-index : 10002; pour que header soit plus haut que le reste (10002 = valeur pour mobile ou site marche. )
### Side pannel et banniere 
Ça me gosse vraiment donc j'ai demandé à ChatGPT plutôt que Codex de m'apprendre comment faire. ChatGPT n'a pas accès au css.main ou au read.me. Donc je vais plus apprendre. 
1. Trouver le media quiery @media dans le css.main 


