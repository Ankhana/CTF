# Phono

#### So we got this file, [whatTheHell](files/whatTheHell.jpg), and this message :

```
Sounds like a melody, no ?

Format : HERO{messageinuppercase}
Author : Thib
```

![whatTheHell](files/whatTheHell.jpg "whatTheHell")

#### It is clear from the description and the shape of the features of the image that the image represents sound. 

#### By doing some research on the internet, we came across this site: https://scape.enepe.fr/steganographie.html

#### This site tells us about some tools to solve steganography challenges. But one of the tools seems very interesting:

![website](images/phono_website.png "website")

#### So we download the application and test on the image. We get a sound file, which gives a sequence of characters : 

#

<audio controls src="files/extracted_audio.wav">
  <p>Votre navigateur ne prend pas en charge l'audio HTML. Voici un
     un <a href="files/extracted_audio.wav">lien vers le fichier audio</a> pour le
     télécharger.</p>
</audio>

#

#### This gives us the following flag: HERO{PH0N0_P4P3R}