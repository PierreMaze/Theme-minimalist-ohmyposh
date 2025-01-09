# 🛠️ Instructions d'installation

### ⚠️ Information importante

**Vous devez exporter le fichier AVANT**

- Exporter le fichier `ThemeMinimalist.omp.json` dans le dossier `User/Username` de votre ordianteur, ensuite faite clique droit et cliquer sur `Copier autant que chemin d'accés`.

## 1️⃣ Créer ou configurer un profil PowerShell

1.  **Ouvrez PowerShell en mode administrateur** :

    - Faites un clic droit sur l’icône PowerShell et sélectionnez **"Exécuter en tant qu’administrateur"**.

2.  **Vérifiez si un profil existe** avec cette commande :  
    `Test-Path $PROFILE`

    - Si la commande retourne `False`, créez un profil avec :  
      `New-Item -Path $PROFILE -ItemType File -Force`

3.  **Ouvrez le fichier de profil** pour le modifier :  
    `notepad $PROFILE`

4.  **Ajoutez la ligne suivante** dans le fichier ouvert pour initialiser OhMyPosh :

    ➡️ Remplacez `C:/User/Username/ThemeMinimalist.omp.json` par l'emplacement de votre fichier de thème _(via clique droit copier chemin d'accés vu plus haut)_.

    ```powershell
    oh-my-posh init pwsh --config C:/User/Username/ThemeMinimalist.omp.json | Out-String | Invoke-Expression
    ```

---

## 2️⃣ Installer OhMyPosh

### Pour Windows

- Ouvrez PowerShell et exécutez :  
  `winget install JanDeDobbeleer.OhMyPosh`

### Pour macOS

- Ouvrez un terminal et exécutez :  
  `brew install oh-my-posh`

### Pour Linux

- Sur un système basé sur Debian/Ubuntu, utilisez :  
  `sudo apt install oh-my-posh`

---

## 3️⃣ Tester l’installation

1. **Vérifiez que OhMyPosh est bien installé** :  
   `oh-my-posh --version`

2. **Appliquez le thème** :
   - Redémarrez votre terminal pour appliquer les modifications.
   - Si nécessaire, refermez et rouvrez votre terminal.

---

## 4️⃣ Installer le thème sur d'autres environnements (facultatif)

### Bash

Ajoutez cette ligne à votre fichier `~/.bashrc` :  
`eval "$(oh-my-posh init bash --config 'chemin/vers/votre-theme.json')"`

### Zsh

Ajoutez cette ligne à votre fichier `~/.zshrc` :  
`eval "$(oh-my-posh init zsh --config 'chemin/vers/votre-theme.json')"`

### Fish

Ajoutez cette ligne à votre fichier `~/.config/fish/config.fish` :  
`oh-my-posh init fish --config 'chemin/vers/votre-theme.json' | source`

---

## 5️⃣ En cas de problème

- **Erreur : "Command not found"**  
  ➡️ Assurez-vous que le dossier contenant OhMyPosh est dans votre `$PATH`.

- **Le thème ne s’affiche pas correctement**  
  ➡️ Vérifiez que vous avez bien installé une police compatible, comme **Fira Code Nerd Font**.

---

# 🖋️ Installer la police Fira Code NT

Pour utiliser la police **Fira Code NT** dans votre terminal et améliorer l'expérience, suivez ces instructions selon votre système d'exploitation.

## 1️⃣ Installer Fira Code NT sur Windows

### Utilisation de Winget (Windows Package Manager)

Si vous avez **Winget** installé, vous pouvez facilement installer **Fira Code NT** en utilisant la commande suivante :

```powershell
winget install --id=FiraCode.FiraCode -e --source winget
```

### Installation manuelle

1. Téléchargez **Fira Code NT** depuis la page officielle [Fira Code GitHub](https://github.com/tonsky/FiraCode) ou [Google Fonts](https://fonts.google.com/specimen/Fira+Code).
2. Décompressez les fichiers téléchargés et faites un clic droit sur les fichiers `.ttf` pour sélectionner **Installer**.

---

## 2️⃣ Installer Fira Code NT sur macOS

### Utilisation de Homebrew (Gestionnaire de paquets macOS)

Si vous n'avez pas **Homebrew** installé, vous pouvez l'installer avec la commande suivante :

```powershell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Ensuite, installez **Fira Code NT** avec :

```powershell
brew tap homebrew/cask-fonts brew install --cask font-fira-code
```

## 3️⃣ Installer Fira Code NT sur Linux

### Utilisation d'apt (Debian/Ubuntu)

Sur les systèmes **Debian/Ubuntu**, vous pouvez installer **Fira Code NT** avec la commande suivante :

```powershell
sudo apt install fonts-firacode
```

### Installation manuelle via Git

1. Clonez le dépôt Fira Code et installez la police manuellement :

```powershell
git clone https://github.com/tonsky/FiraCode.git
cd FiraCode
sudo mv ttf/* /usr/share/fonts/truetype/
sudo fc-cache -fv
```

---

## 💡 Bonus : Comment vérifier si la police a été installée correctement

1. Ouvrez n'importe quel éditeur de texte (comme VSCode, Sublime Text, ou votre terminal).
2. Tapez du code ou du texte qui inclut des ligatures, comme `let x = 100;` (cela affichera des ligatures dans certains éditeurs).
3. Si les ligatures apparaissent comme prévu, cela signifie que la police est installée et fonctionne correctement !

---
