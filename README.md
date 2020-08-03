# Ensemble de playbooks Ansible pour configurer des environnements

## Étape 1 — Installation d'Ansible
Se placer dans le répertoire racine et lancer l'installation d'Ansible:
```
/bin/bash ansible-install.sh
```

## Étape 2 — Vérification de l'inventaire des machines
Modifier (si nécessaire) les fichiers d'inventaire, par exemple:
```
nano inventories/ubuntu_20.04_desktop_computer_inventory
```

## Étape 3 — Lancer le playbook
Lancer un playbook, par exemple:
```
ansible-playbook -i inventories/ubuntu_20.04_desktop_computer_inventory playbooks/ubuntu_20.04_desktop_computer_install.yml --ask-become-pass
```
**Note:** 
- Le "become pass" est votre mot de passe administrateur qui est requis par certaines commandes.
- L'option "-vvv" peut être utilisée pour le débugage.

## Étape 4 — Monter les disques
Si nécessaire, monter les disques:
```
sudo mount -a
```

# Playbooks

## Installation d'une machine locale préconfigurée pour le développement
Fichier: **ubuntu_20.04_desktop_computer_install.yml**
