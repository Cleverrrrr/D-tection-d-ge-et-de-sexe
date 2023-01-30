# Detection d'âge et de sexe  


<h2>Objectif :</h2>
<p>Construire un détecteur de genre et d'âge qui peut deviner approximativement le genre et l'âge de la personne (visage) dans une image ou via une webcam.</p>

<h2>Données :</h2>
<p>Pour ce projet Python, j'ai utilisé le jeu de données Adience; le jeu de données est disponible dans le domaine public et vous pouvez le trouver <a href="https://www.kaggle.com/ttungl/adience-benchmark-gender-and-age-classification">ici</a>. Ce jeu de données sert de référence pour les photos de visage et inclut diverses conditions d'imagerie du monde réel telles que le bruit, l'éclairage, la pose et l'apparence. Les images ont été collectées à partir d'albums Flickr et distribuées sous la licence Creative Commons (CC). Il comporte un total de 26 580 photos de 2 284 sujets dans huit intervalles d'âge et pèse environ 1 Go. Les modèles que j'ai utilisés ont été formés sur ce jeu de données.</p>
<h2>Bibliothèques Python supplémentaires requises :</h2>
<ul>
  <li>OpenCV</li>
  
       pip install opencv-python
</ul>
<ul>
 <li>argparse</li>
  
       pip install argparse
</ul>

<h2>Le contenu du Project :</h2>
<ul>
  <li>opencv_face_detector.pbtxt</li>
  <li>opencv_face_detector_uint8.pb</li>
  <li>age_deploy.prototxt</li>
  <li>age_net.caffemodel</li>
  <li>gender_deploy.prototxt</li>
  <li>gender_net.caffemodel</li>
  <li>quelques images pour essayer le projet</li>
  <li>detect.py</li>
 </ul>
  <p>Pour la détection de visage, nous avons un fichier .pb - il s'agit d'un fichier protobuf (protocol buffer); il contient la définition de graphe et les poids entraînés du modèle. Nous pouvons utiliser cela pour exécuter le modèle entraîné. Et alors qu'un fichier .pb contient le protobuf en format binaire, celui avec l'extension .pbtxt le contient en format texte. Ce sont des fichiers TensorFlow. Pour l'âge et le genre, les fichiers .prototxt décrivent la configuration du réseau et le fichier .caffemodel définit les états internes des paramètres des couches.</p>
 
 <h2>Utilisation :</h2>
 <ul>
  <li>Téléchargez mon dépôt</li>
  <li>Ouvrez votre invite de commande ou votre terminal et changez de répertoire vers le dossier où se trouvent tous les fichiers.</li>
  <li><b>Détection du genre et de l'âge du visage dans une image</b> Utilisez la commande :</li>
  
      python detect.py --image <image_name>
</ul>
  <p><b>Note: </b>L'image doit être présente dans le même dossier où se trouvent tous les fichiers</p>
<ul>
  <li><b>Détection du genre et de l'âge du visage à travers la webcam</b> Utilisez la commande :</li>
  
      python detect.py
</ul>
<ul>
  <li>Appuyez sur <b>Ctrl + C</b> pour arrêter l'exécution du programme.</li>
</ul>


<h2>Exemple :</h2>

    
    >python detect.py --image man2.jpg
    Gender: Male
    Age: 25-32 years
    
<img src="Example/Detecting age and gender man2.png">
