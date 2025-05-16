Contenu initial dans main d'un fichier que nous nommerons conflits.md

Je crée une nouvelle branche, et je me positionne dessus.

```bash
git checkout -b bugfix/conflit
```

Maintenant j'édite ce fichier conflits.md depuis la branche bugfix/conflit, et je commit.

Ensuite, on revient sur la branche main.

```bash
git checkout main
```

### Edition depuis main à nouveau

Tiens tiens, mais où est ce que je viens de faire ? Oulala, ça se complique cette affaire !?

Tant pis je commit, et ensuite je tente une fusion de mes deux branches.

```bash
git add conflits.md
```

```bash
git commit -m "edition depuis main"
```

Ok ma version main est mise à jour.

Maintenant, je tente la fusion qui doit entraîner un conflit, avec 

```bash
git merge bugfix/conflits
```

### Le résultat du merge rpopose de régler les soucis de merge dans l'éditeur de texte utilisé

```bash
nano conflits.md
```

On corrige et on enregistre.

Et donc stagge et on commit avec un beau message.

*La marteau thérapie y a que ça de vrai !*