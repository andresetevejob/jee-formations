# Configuration de votre environnement de travail

Pré-requis:
-----------
- Java SE 17
- Maven 3
- Eclipse Java EE Developer
- Widfly 27


I - Configuration de la JDK dans Eclipse.
-----------------------------------------

Depuis le menu Window > preferences. Selectionner l'élément Java > Installed JRE. Cliquez ensuite sur le bouton add. Vous verrez apparaître une fenêtre comme sur la capture ci-dessous.Cliquez enfin sur le bouton next


![ScreenShort](assets/jdk-step-1.png)





Cliquez sur le bouton add pour definir votre JVM.
- Selectionnez le chemin de votre JDK au moyen du bouton directory du formualire
- Nommez votre JRE, dans le champ JRE Name


![ScreenShort](assets/jdk-step-2.png)





Une fois selectionné vous devriez avoir un resultat similaire, à celui affiché par l'ecran ci-dessous


![ScreenShort](assets/jdk-step-3.png)




Enfin cochez votre JVM dans la liste ci-dessous


![ScreenShort](assets/jdk-step-4.png)






III - Configuration de maven.
----------------------------------------

Depuis le menu Window > preferences. 

Selectionnez l'élément installation en dessous du menu maven et cliquez ensuite sur le bouton add. Enfin au moyen du bouton directory selectionnez le repertoire d'installation de maven et donnez un nom à votre installation cliquez sur le bouton finish et selectionnez votre element dans la liste des éléments maven affichés comme sur la capture d'écran.

![ScreenShort](assets/maven.png)


III - Configuration du serveur Widfly.
----------------------------------------

Depuis l'onglet Servers d'Eclipse (Pour le faire apparaître allez dans Window > show view > Servers). Cliquez sur le lien create a new server

![ScreenShort](assets/server-step-1.png)









Deroulez le dossier JBoss Community et choisissez le serveur Widfly 24+ et cliquez ensuite sur le bouton next
![ScreenShort](assets/server-step-2.png)




Assurez vous que vous avez les éléments selectionnées comme sur la capture d'écran et ensuite cliquez sur le bouton next


![ScreenShort](assets/server-step-3.png)





Enfin nommez votre serveur et selectionnez son chemin d'installation au moyen du bouton browse


![ScreenShort](assets/server-step-4.png)