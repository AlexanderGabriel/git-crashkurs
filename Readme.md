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


# branches

# tags

# mergen

#gitignore

#advanced

##submodules

# sonstiges
