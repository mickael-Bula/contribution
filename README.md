# WORKFLOW GIT

Ne JAMAIS coder sur la branche ```main```
A chaque nouvelle fonctionnalité créer une branche dédiée :
```bash
git pull origin main
git checkout -b newFeature
```

Sur cette branche on développe librement, on commit régulièrement et on push quotidiennement - minimum :
```bash
git add .
git commit -m "mon message de commit"
```

Une fois satisfait de son code ou en cas de problème on le pousse sur la branche du même nom (surtout pas main !)
```bash
git push -u origin newFeature
```

On peut alors faire une pull request sur Github.
Une fois celle-ci acceptée (après review et corrections éventuelles), il faut la fusionner dans le code de référence.
Pour cela, le développeur doit s'assurer d'être à jour avec la branche principale :
```bash
git checkout main
git pull origin main
```
S'il n'y a pas de conflit, on peut fusionner en local puis sur le remote :
```bash
git merge newFeature
git push origin main
```
Puisque le code commun a changé, il peut être bon que chaque développeur mette à jour la branche commune :
```bash
git checkout main
git pull origin main
```
