### H7N-NSI #01

~ Kensuke Koike Pyxelator ~

L'artiste contemporain japonais Kensuke Koike (https://www.kensukekoike.com/) est connu pour ses manipulations de photographie anciennes. Il décompose les images pour en créer de nouvelles. Plusieurs de ses travaux sont présentés dans ces articles : [www.bewaremag.com](https://www.bewaremag.com/kensuke-koike/) & [www.pen-online.com](https://pen-online.com/fr/arts/kensuke-koike-alchimiste-de-la-photo-detournee/). Son compte Twitter : [@k_koi](https://twitter.com/k_koi). Son site internet : https://www.kensukekoike.com/.

#### But
Faire en Python ce que Kensuke Koike fait à la main.

#### Sujet
Analyser les oeuvres de Kensuke Koike ci-dessous (images et vidéos) et choisir une technique à réaliser en Python (attention, certaines sont plus difficiles que d'autres à implémenter). Les images à manipuler avec le code Python sont dans le dossier "images" (https://github.com/hackathon-nsi/h7n-nsi-01/images).

#### Consignes
* rédiger la documentation de votre projet dans le fichier README.md (présenter la technique choisie, décrire la démarche, expliquer le code...)
* placer le code Python dans un ou plusieurs fichiers .py
* commenter le code


**IMAGES**

**Technique 1**

![voir](https://raw.githubusercontent.com/hackathon-nsi/h7n-nsi-01/main/kk-01.png)

**Technique 2**

![voir](https://raw.githubusercontent.com/hackathon-nsi/h7n-nsi-01/main/kk-02.png)

**Technique 3**

![voir](https://raw.githubusercontent.com/hackathon-nsi/h7n-nsi-01/main/kk-03.png)

**Technique 4**

![voir](https://raw.githubusercontent.com/hackathon-nsi/h7n-nsi-01/main/kk-04.png)

**VIDEOS**

**Technique 5**

[![voir](https://img.youtube.com/vi/U1KiC0AXhHg/maxresdefault.jpg)](https://youtu.be/U1KiC0AXhHg)

**Technique 6**

[![voir](https://img.youtube.com/vi/f1fXCRtSUWU/maxresdefault.jpg)](https://youtu.be/f1fXCRtSUWU)

**Technique 7**

[![voir](https://img.youtube.com/vi/As2KMSOad08/maxresdefault.jpg)](https://youtu.be/As2KMSOad08)

**Technique 8**

[![voir](https://img.youtube.com/vi/GhR0J9Yjd8Q/maxresdefault.jpg)](https://youtu.be/GhR0J9Yjd8Q)


#### Aide
En Python, la bibliothèque PIL permet de manipuler les images :

```python
from PIL import Image
from IPython.display import display
import urllib.request
 
# ouvrir une image hébergée sur internet
im = Image.open(urllib.request.urlopen('https://raw.githubusercontent.com/nsi-lfitokyo/kensuke-koike-pyxelator/master/champ-coquelicots.bmp'))
 
# créer une nouvelle image vide
# le deuxième argument représente la taille de l'image et le troisième argument (optionnel) la couleur de remplissage au format RVB
im_new = Image.new("RGB", (512, 512), (128, 128, 128))
 
# informations sur l'image
print(im.format, im.size, im.mode)
 
# taille de l'image
width, height = im.size 
 
# valeurs du pixel de coordonnées x, y (l'origine (0, 0) est en haut à gauche)
pixel = im.getpixel((x, y))
 
# valeurs des couleurs rouge, vert, bleu
p_rouge = pixel[0]
p_vert =  pixel[1]
p_bleu =  pixel[2]
 
# modification du pixel de coordonnées x, y
im.putpixel((x,y),(r,g,b))
 
# affichage de l'image
display(im)
```
