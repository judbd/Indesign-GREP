#Expressions GREP utiles dans indesign

####Espace fine entre les guillemets français
Chercher : («\s*)(.*?)(\s*»)
Remplacer par : «~<$2~<»

####Rechercher/Formater les lettres "RT" dans un copier/coller de tweet
GREP : \bRT(?=\s@)
(toutes les occurences de "RT" suivies directement par un espace et un arobase)

####Formater les lettres "RT" + le nom d'utilisateur et les 2 points dans un copier/coller de tweet
GREP : \bRT\s@\w+:?
(toutes les occurences de "RT" + l'espace et le nom d'utilisateur ainsi que les 2 points)

####Rechercher/Formater les noms d'utilisateur twitter
GREP : (?<!\w)@\w+
(@ suivi d'un mot sans rien devant pour éviter la sélection d'emails)

####Rechercher/Formater les hashtags twitter
GREP : (?<!\w)#\w+
(# suivi d'un mot sans rien devant)
