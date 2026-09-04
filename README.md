<img width="955" height="696" alt="Capture d’écran du 2026-09-04 21-23-16" src="https://github.com/user-attachments/assets/6498f73d-e8d5-423d-a537-330f9dccafbd" />
# Comp' — Git Companion
Git without the Git headache.

A tiny desktop GUI for people coding with AI assistants who don't want to manage Git from a terminal.

Select a project → see what changed → commit → pull → push.

Linux, mas OS today. Windows next.


**[⬇ Télécharger la dernière version](../../releases/latest) · [⬇ Download the latest version](../../releases/latest)**

*[Français](#français) · [English](#english)*

---

## Français

Comp' est une petite application de bureau posée au-dessus de Git, pour les personnes
qui développent avec Claude Desktop ou Codex Desktop et ne veulent pas passer par un
terminal. Elle gère plusieurs projets locaux, rend leur état Git lisible d'un coup
d'œil, et protège les opérations de synchronisation risquées.

Ce n'est ni un éditeur, ni un IDE, ni un client d'agent. Elle ne lance aucun agent et
n'envoie jamais de code toute seule.

### Ce dépôt ne contient pas de code

Vous êtes sur le dépôt de **distribution**. Il ne sert qu'à héberger les applications
prêtes à l'emploi ; le code source vit ailleurs et reste privé.

Les fichiers à télécharger ne sont donc pas dans la liste ci-dessus, mais dans
l'onglet **[Releases](../../releases)**. Chaque plateforme a sa propre suite de
versions : corriger le Mac ne réédite pas la version Ubuntu.

| Plateforme | Fichier | Remarque |
|---|---|---|
| macOS Apple Silicon | `Comp-macOS-Apple-Silicon-<version>.zip` | macOS 12 minimum |
| macOS Intel | `Comp-macOS-Intel-<version>.zip` | macOS 12 minimum |
| Ubuntu x86_64 | `Comp-Ubuntu-x86_64-<version>.tar.gz` | construit sur Ubuntu 22.04 |

### Installer sur macOS

Décompressez l'archive, puis glissez `Comp.app` dans votre dossier Applications.

L'application **n'est pas signée par Apple**. Au premier lancement, un double-clic
affiche donc un refus. Faites un **clic droit sur Comp' → Ouvrir**, puis confirmez :
macOS s'en souvient et les lancements suivants sont ordinaires.

### Installer sur Ubuntu

```bash
tar -xzf Comp-Ubuntu-x86_64-<version>.tar.gz
./Comp/Comp
```

Git doit être installé sur la machine : Comp' s'appuie dessus et ne l'embarque pas.
Sur un bureau ordinaire, les bibliothèques graphiques nécessaires sont déjà là ; sur
une machine sans environnement de bureau, installez `libegl1` et `libxkbcommon-x11-0`.

### Vérifier le téléchargement

Chaque release contient un fichier `SHA256SUMS.txt`. Placez-le à côté des archives
téléchargées et lancez :

```bash
sha256sum --check SHA256SUMS.txt      # Linux
shasum -a 256 -c SHA256SUMS.txt       # macOS
```

### Vos identifiants restent chez vous

Comp' ne demande, ne lit et ne stocke **aucun mot de passe ni aucun token**.
L'authentification GitHub est déléguée à l'outil officiel GitHub CLI, ou à la
configuration Git et SSH déjà présente sur votre ordinateur.

---

## English

Comp' is a small desktop application sitting on top of Git, for people who build with
Claude Desktop or Codex Desktop and would rather not open a terminal. It handles
several local projects, makes their Git state readable at a glance, and guards the
synchronisation steps that can go wrong.

It is not an editor, an IDE, or an agent client. It runs no agent and never sends
code on its own.

### This repository holds no source code

You are on the **distribution** repository. It exists only to host the ready-to-run
applications; the source code lives elsewhere and stays private.

So the downloads are not in the file list above — they are under the
**[Releases](../../releases)** tab. Each platform has its own series of versions:
fixing the Mac build does not reissue the Ubuntu one.

| Platform | File | Note |
|---|---|---|
| macOS Apple Silicon | `Comp-macOS-Apple-Silicon-<version>.zip` | macOS 12 or later |
| macOS Intel | `Comp-macOS-Intel-<version>.zip` | macOS 12 or later |
| Ubuntu x86_64 | `Comp-Ubuntu-x86_64-<version>.tar.gz` | built on Ubuntu 22.04 |

### Installing on macOS

Unzip the archive, then drag `Comp.app` into your Applications folder.

The application is **not signed by Apple**, so a double click is refused the first
time. Instead, **right-click Comp' → Open**, then confirm: macOS remembers, and every
later launch is ordinary.

### Installing on Ubuntu

```bash
tar -xzf Comp-Ubuntu-x86_64-<version>.tar.gz
./Comp/Comp
```

Git must be installed on the machine: Comp' relies on it and does not bundle it. On an
ordinary desktop the graphics libraries are already there; on a machine with no desktop
environment, install `libegl1` and `libxkbcommon-x11-0`.

### Verifying your download

Every release ships a `SHA256SUMS.txt`. Put it next to the downloaded archives and run:

```bash
sha256sum --check SHA256SUMS.txt      # Linux
shasum -a 256 -c SHA256SUMS.txt       # macOS
```

### Your credentials stay with you

Comp' asks for, reads and stores **no password and no token**. GitHub authentication
is delegated to the official GitHub CLI, or to the Git and SSH configuration already
present on your computer.
