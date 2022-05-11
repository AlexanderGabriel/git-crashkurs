# Git-Crashkurs
Notizen zum Git-Crashkurs

# einrichten
E-Mail und Name
CRLF-Zeugs

# init
Neues Repository anlegen:
git init PATH
z.B. git init git-crashkurs

# klonen
holt ein remote-repository lokal, damit darin programmiert werden kann
git clone https://github.com/AlexanderGabriel/git-crashkurs

# stagen und committen
stagen speichert Änderungen zwischen, ohne einen neuen Eintrag ins Log zu machen.
So kann Arbeit Zwischengespeichert werden und ist dann im Diff auch nicht mehr sichtbar

git add dateiname

committen erzeugt einen neuen Eintrag im Log, also einen Patch, der alle bisher gestagten Änderungen beinhaltet

git commit -m "NACHTRICHT"

# remotes (mehrere)
ein zentrales Repository heißt "Remote"
Remote hinzufügen: git remote add origin https://github.com/AlexanderGabriel/git-crashkurs
Angeben, welcher Origin der Upstream für den Main-Branch ist und gleichzeitig pushen
git push --set-upstream origin main

normlaes pushen:
git push

git remote add MarcoFirsching https://github.com/marcofirsching/git-crashkurs
git fetch MarcoFirsching 
git pull MarcoFirsching main

# pushen und pullen
git pull holt vom remote die Änderungen vom aktuellen Branch in den lokalen branch
git pull MarcoFirsching main

git push schiebt die Änderungen wieder ins remote-Repository

# branches
Branch erstellen:
git branch NAME

Branch auschecken:
git checkout BRANCHNAME

Auf welchem Branch bin ich?
git branch

Branch veröffentlichen:
git push --set-upstream origin AenderugenAlex


# auschecken

git checkout BRANCHNAME

git checkout TAGNAME

git checkout REVISIONS-Prüfsumme

# tags
Erstellt Tags/Releases/Markierungen, damit man einfacher zu einem bestimmten Stand zurückwechseln kann
z.B.:
git tag v1.0


# mergen

Branch zusammenführen.
Zuerst alles committen.
Dann auf den Branch wechseln, der die Änderungen empfangen soll:
git checkout main
Dann den Branch zusammenführen (also die Änderungen herholen):
git merge AenderungenAlex

# .gitignore
Dateien oder Dateimuster hier eintragen.
Diese Dateien werden von Git ignoriert

z.B:
config.php
*.xml
.env

# advanced

## submodules
Untermodul hinzufügen:
git submodule add https://gogs.digital-infinity.de/DigitalInfinity/ansible-role-acme.sh

Wird wie ein eigenes Repository behandelt aber das übergeordnete Repository weiß von dem Untermodul und auch,
welchen Commit es verwenden soll

# sonstiges

## Pull-Request

Einen Branch erstellen, diesen veröffentlichen und dann über Github "beantragen", dass die Änderungen ins
Urspüngliche Repository (oder ein anderer Branch) übernommen werden

# Besonderheiten
leere Verzeichnisse gibt es im Git nicht