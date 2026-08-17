# Awesome OpenSource Collection

Une collection soigneusement sélectionnée des meilleurs projets et logiciels libres (Open Source). 
Ce dépôt ne se contente pas d'être une simple liste : il intègre une **interface web interactive** permettant de filtrer, découvrir et installer facilement des dizaines d'outils pour le Self-hosting, le Développement, le Multimédia et l'Optimisation Système.



## Fonctionnalités de l'interface

* **Recherche et Filtres avancés** : Triez par tags, plateformes (Linux, Windows, Web, etc.), licences ou gestionnaires de paquets (Pacman, Flatpak, Docker, APT...).
* **Copie rapide des commandes** : Un clic sur un paquet génère et copie instantanément la commande d'installation exacte (ex: `sudo pacman -S btop`).
* **Génération de script Bash** : Sélectionnez les logiciels que vous avez installés (✔️), et générez un script d'installation complet (regroupant intelligemment Pacman, AUR, Flatpak et Docker).
* **Personnalisation** : Thèmes dynamiques (Clair, Sombre, OLED) et 8 couleurs d'accentuation au choix.
* **Sauvegarde locale** : Vos favoris (👁️ Connus, ✔️ Installés) et votre thème sont automatiquement sauvegardés dans votre navigateur.

## Comment démarrer

### Option 1 : Voir en ligne (Recommandé)
Le projet est déployé et accessible directement via GitHub Pages :
[https://hoferlukaslh.github.io/Awesome-OpenSource/](https://hoferlukaslh.github.io/Awesome-OpenSource/)

### Option 2 : Exécuter en local
Si vous avez cloné ou téléchargé ce dépôt, vous ne pouvez pas ouvrir directement le fichier `index.html` à cause des sécurités du navigateur (CORS) bloquant la lecture du fichier JSON local.
Lancez simplement un serveur web local depuis le dossier du projet :

```bash
python3 -m http.server
```

Puis, ouvrez http://localhost:8000 dans votre navigateur web.

## Comment contribuer / Ajouter un logiciel
Toutes les données sont séparées de l'interface. Pour ajouter un nouveau logiciel, il n'y a pas besoin de toucher au code HTML.
Il suffit d'éditer le fichier awesome_opensource.json et d'y ajouter un nouveau bloc en respectant ce format :


```json
{
  "name": "Nom du logiciel",
  "category": "Catégorie",
  "description": "Courte description.",
  "license": "MIT",
  "platforms": ["Linux", "Windows", "Web"],
  "packages": {
    "flatpak": "nom.du.paquet",
    "docker": "image/nom:latest"
  },
  "url": "[https://lien-officiel.com](https://lien-officiel.com)",
  "logo": "[https://icon.horse/icon/domaine.com](https://icon.horse/icon/domaine.com)",
  "tags": ["Tag1", "Tag2"]
}
```

L'interface web se mettra à jour automatiquement, triera le logiciel par ordre alphabétique, et générera les tags dynamiquement !
