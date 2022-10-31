## Hello World TP - Jakarta EE
------------------------------
Ce tp a pour but de nous permettre de réaliser notre première application servlet avec la plateforme Jakarata EE

Pré-requis:
-----------
- Java SE 17
- Maven 3
- Eclipse Java EE Developer
- Widfly 27

## Création du projet
1 - Depuis le menu File > New > Maven project. Créer un nouveau project maven.

![ScreenShort](assets/project-step-1.png)













vous obtiendrez un écran comme sur la capture ci-dessus.Cochez les deux options comme sur la capture et cliquez sur le bouton next.

2 - Remplissez le formulaire comme sur la capture ci-dessous

- Group Id: com.nextu.jakartaee 
- Artifact Id: servlet
- Packaging: war 

![ScreenShort](assets/project-step-2.png)


3 - Modification du pom.xml du projet.

Rajoutez les lignes ci-dessous dans le pom de votre projet (sur la capture d'écran le nom du fichier est en surbrillance)
````
<properties>
     <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
     <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
     <maven.compiler.source>17</maven.compiler.source>
     <maven.compiler.target>17</maven.compiler.target>
     <failOnMissingWebXml>false</failOnMissingWebXml>
  </properties>

   <dependencies>
  <dependency>
       <groupId>jakarta.platform</groupId>
       <artifactId>jakarta.jakartaee-api</artifactId>
       <version>10.0.0</version>
       <scope>provided</scope>
  </dependency>
  </dependencies>
  <build>
    <plugins>
    	 <plugin>
          <artifactId>maven-war-plugin</artifactId>
          <version>3.2.2</version>
        </plugin>
    </plugins>
  </build>
````



![ScreenShort](assets/project-step-3.png)

4- Création de package :
Cliquez droit sur l'élément src/main/java

![ScreenShort](assets/project-step-4.png)



Nommez le package comme sur la capture d'écran

![ScreenShort](assets/project-step-5.png)


5- Ajouter un descripteur de deploiement web.xml

![ScreenShort](assets/project-step-6.png)

6- Vous devez obtenir un nouveau fichier web.xml, généré par Eclipse.

![ScreenShort](assets/webxml.png)


7- Création de la servlet.
Cliquez droit sur le nom du package précédemment crée.

![ScreenShort](assets/project-step-7.png)



Nommez la servlet, comme sur la capture ci-dessous.
![ScreenShort](assets/project-step-8.png)



Definissez l'url de votre servlet (de préférence pas d'acccent et en miniscule)

![ScreenShort](assets/project-step-9.png)



Cochez les éléments comme sur la capture d'écran ci-dessous
![ScreenShort](assets/project-step-10.png)


8- Correction des noms de package.
Une fois votre servlet généré, des erreurs apparaissent en rouge.
Modifiez les imports de classe indiquez en rouge par celles-ci dessous (Pour les voir cliquez sur le bouton + de la ligne 3 dans la zone de code, ce bouton permet de derouler les imports )

````
import jakarta.servlet.ServletException;
import jakarta.servlet.http.HttpServlet;
import jakarta.servlet.http.HttpServletRequest;
import jakarta.servlet.http.HttpServletResponse;

````
![ScreenShort](assets/project-step-11.png)


10 - Notre première ligne de code.

Configurer le compilateur Java du projet.Faites un clique droit sur votre projet.Selectionnez la version 17 de java SE comme sur la capture d'écran.

![ScreenShort](assets/compiler.png)



Supprimez, le contenu de votre méthode doGet, pour la remplacer par celle-ci

````
		PrintWriter out = response.getWriter();
		String html = """
	              <html>
	                  <body>
	                      <p>Hello, world</p>
	                  </body>
	              </html>
	              """;
		out.println(html);
````

11 - Construction du projet

Configuration de la commande  de build.Depuis le menu Run d'eclipse

![ScreenShort](assets/run.png)


Créer une nouvelle configuration maven, en faisant un clique droit sur l'element maven

![ScreenShort](assets/create-run.png)


Remplissez le formulaire comme sur l'écran ci-dessous
````
Base directory : ${project_loc:servlet} (servlet correspond au nom du projet dans Eclipse)
Goals : package

User settings: correspond à l'endroit ou se trouve votre fichier settings.xml dans maven

````

![ScreenShort](assets/fill-form-run.png)


Cliquez enfin sur le bouton run.si tout se passe bien, vous devriez obtenir un resultat positif comme celui de la capture ci-dessous


![ScreenShort](assets/build_result.png)



12 - Dans l'onglet server d'Eclipse, faites un clique droit sur le serveur et selectionnez l'option add/remove

![ScreenShort](assets/add-project.png)


13 - Selectionnez votre projet et deplacer vers la droit au moyen du bouton add et cliquez sur finish

![ScreenShort](assets/add-project-2.png)


14 - Demarrez le serveur. Cliquez droit sur votre serveur et ensuite cliquez sur sur bouton start qui apparâit dans le menu contextuel.

![ScreenShort](assets/start-server.png)

15 - Vous devriez avoir les logs suivantes, et cette ligne indiquant que votre application est bien démarré

![ScreenShort](assets/server_log.png)


16 - Ouvrez le navigateur de votre choix et saisissez l'url suivante : http://localhost:8080/servlet-0.0.1-SNAPSHOT/helloworld

Vous devriez voir s'afficher à l'écran , la page ci-dessous:

![ScreenShort](assets/rs.png)
