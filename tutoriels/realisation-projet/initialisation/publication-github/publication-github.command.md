
# 1. Vérifier l'authentification
gh auth status

# 2. Se connecter si nécessaire
gh auth login

# 3. Créer le projet
mkdir blog-des-laureats
cd blog-des-laureats

# 4. Créer .gitignore vide
New-Item .gitignore -ItemType File

# 5. Initialiser Git
git init

# 6. Créer la branche sprint1
git checkout -b sprint1

# 7. Créer l'arborescence
mkdir -Force tutoriels/realisation-projet/initialisation/publication-github

# 8. Créer le journal des commandes
New-Item -ItemType File -Path tutoriels/realisation-projet/initialisation/publication-github/publication-github.command.md

# 9. Ajouter les fichiers
git add .gitignore tutoriels/realisation-projet/initialisation/publication-github/publication-github.command.md

# 10. Vérifier les fichiers
git status

# 11. Créer le premier commit
git commit -m "feat: initialisation du projet et journal des commandes"

# 12. Vérifier le commit
git log --oneline

# 13. Publier sur GitHub
gh repo create

# 14. Vérifier le remote
git remote -v

# 15. Vérifier la branche
git branch --show-current

# 16. Vérifier l'état final
git status
