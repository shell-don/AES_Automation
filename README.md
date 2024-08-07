# AES Automation
Permet de chiffrer et déchiffrer (Comming Soon) n fois un fichier en AES-256 de manière simple et intéractive en local. Codé en BASH.

## Installation
(Mac)

Installez [Aescrypt](https://www.aescrypt.com/download/) en mode console pour votre machine. 

Installez Keepassxc avec votre gestionnaire de paquet préféré.
```zsh
brew install keepassxc
```
Créer un fichier sur votre bureau appelé AES_Automation.
```zsh
mkdir ~/desktop/AES_Automation
```
Copiez aescrypt (console-M1/M2) dans le dossier, commande sous cette forme :
(à modifier si vous n'avez pas télécharger la même version)
```bash
cp ~/Downloads/aescrypt_mac_v316_m1m2/usr/local/bin/aescrypt ~/desktop/AES_Automation 
```
Téléchargez le ZIP de ce github puis éxécutez : 
```bash
cp ~/Downloads/AES_Automation-main/Bêta/bc.sh ~/desktop/AES_Automation ; cp ~/Downloads/AES_Automation-main/Bêta/bcr.sh ~/desktop/AES_Automation ; chmod +x  ~/desktop/AES_Automation/bc.sh ; chmod +x  ~/desktop/AES_Automation/bcr.sh
```
Enfin exportez le chemin du dossier dans le PATH pour pouvoir les éxécuter.
```bash
export PATH=$PATH:~/desktop/AES_Automation
```
Supprimer les fichiers télécharger, AES_Automation possède le nécessaire.
### Optimisations
(optionnel)
Ajoutez cette fonction dans ~/.zshrc ou ~./.bashrc pour retrouver les alias à chaque lancement du terminal.
```bash
if [[ -r ~/.aliasrc ]]
  then
  . ~/.aliasrc
fi
```

Ajoutez deux alias dans ~/.aliasrc (dédié aux alias)
```zsh
alias bc="bc.sh"
alias bcr="bcr.sh"
```

## Usage
Lancer le chiffrement d'un fichier :
```bash
. bc.sh
```
Lancer le déchiffrement d'un fichier :
```zsh
bcr.sh
```
## Coming Soon

Résolution "Error: Message has been altered or password is incorrect"
Pour le déchiffrement l'erreur peut venir de l'adresse HMAC qu'aescrypt fourni automatiquement pendant le chiffrement. Le mot de passe est le bon (vérifié à la main). Cependant même en faisant des tests en modifiant le code source d'aescrypt, soit le message d'erreur perssiste soit le fichier n'est pas déchiffré (fichier vide). 
Si vous avez une idée pour la résoudre contactez moi.

En attendant cet outil peut être utilisé pour supprimer de manière sécuriser un fichier. 
