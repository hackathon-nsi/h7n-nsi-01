**H7N.NSI #01**

~ Kensuke Koike Pyxelator ~

L'artiste visuel contemporain Kensuke Koike (https://www.kensukekoike.com/) manipule les images pour leur donner une autre vie. Plusieurs de ses travaux sont présentés dans cet article : https://www.bewaremag.com/kensuke-koike/.


En informatique il existe deux grandes catégories d'images : les images vectorielles et les image matricielles. Parmi les images matricielles, il existe plusieurs formats : les formats compressés comme les formats jpg et png et des formats non compressés comme les formats bmp et tiff. Pour simplifier la manipulation des images, nous allons utiliser le format non compressé `bmp`.

But  : faire en Python ce que l'artisite japonais, Kensuke Koike, fait à la main.


Sujet  : Analysez les oeuvres de Kensuke Koike ci-dessous et choisir une tehcnique à réaliser en Python. Les imqges que vous qvez le droit dùutiliser sont dans le dossier "images".

Méthode de travail : dans le repertoire GitHub de votre equipe, completer le fichier README.md et place un ou plusieurts fichier en .py qui contiendront le code Python.

Consignes :
utilsier les chemn absolus pour les images





Exemple et aide :

En Python, la bibliothèque PIL permet de manipuler les images :
'''python
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
 
# sauvegarde locale de l'image
new_im.save('image_mod.bmp')
'''






