Expressions GREP utiles dans indesign
======

######Espace fine entre les guillemets français

* __Chercher :__ `(«\s*)(.*?)(\s*»)`
* __Remplacer par :__ `«~<$2~<»`

---

######Espace fine devant la double ponctuation

* __Chercher :__ `(\s(!|\?|:))`
* __Remplacer par :__ `~<$2`

---

######Trois points (ou plus) consécutifs en ellipse

* __Chercher :__ `\.{3,}`
* __Remplacer par :__ `…`

(au moins 3 points remplacés par une ellipse)

---

######Rechercher/Formater les lettres "RT" dans un copier/coller de tweet

* __GREP :__ `\bRT(?=\s@)`

(toutes les occurences de "RT" suivies directement par un espace et un arobase)

---

######Formater les lettres "RT" + le nom d'utilisateur et les 2 points dans un copier/coller de tweet

* __GREP :__ `\bRT\s@\w+:?`

(toutes les occurences de "RT" + l'espace et le nom d'utilisateur ainsi que les 2 points)

---

######Rechercher/Formater les noms d'utilisateur twitter

* __GREP :__ `(?<!\w)@\w+`

(@ sans rien devant suivi d'un mot pour éviter la sélection d'emails)

---

######Rechercher/Formater les hashtags twitter

* __GREP :__ `(?<!\w)#\w+`

(# sans rien devant suivi d'un mot)
