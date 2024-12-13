# Exam Final - Développement Android Studio

Ce projet est une démonstration des compétences en développement Android avec des exemples de débogage, de gestion d'exceptions, et de tests (unitaires et UI). Vous trouverez ci-dessous des informations détaillées sur les étapes du projet.

---

## Table des matières

1. [Structure du projet](#structure-du-projet)
2. [Instructions pour exécuter le projet](#instructions-pour-exécuter-le-projet)
3. [Captures d'écran](#captures-décran)
4. [Fonctionnalités](#fonctionnalités)
5. [Tests](#tests)
6. [Installation et exécution](#installation-et-exécution)

---


## Instructions pour exécuter le projet

1. **Cloner le projet** :
   ```bash
   git clone https://github.com/salambaye/Exam-Final-Aprem.git
   cd Exam-Final-Aprem

2. **Ouvrir le projet dans Android Studio** :
- Sélectionnez le fichier build.gradle dans le répertoire racine.

4. **Exécuter l'application** :
- Connectez un appareil ou démarrez un émulateur Android.
- Cliquez sur Run > Run 'app' ou utilisez le raccourci Shift + F10.

---

## Captures d'écran
### Débogage avec Logcat :
![Capture d'écran de l'application](C:\Users\DELL\Pictures\debogage1.png)

### Gestion des exceptions :

### Points d’Arrêt et Inspection 


---
## Fonctionnalités

1.  **Débogage avec Logcat** :
      - Ajout de journaux (logs) pour suivre le comportement de l'application.
      - Exemple :
      ```bash
      Log.d("MainActivity", "Application démarrée")

3. **Gestion des exceptions courantes** :
        - Gestion des exceptions telles que NullPointerException et IndexOutOfBoundsException.
        - Utilisation de vérifications avant l'accès aux données.

4. **Interface utilisateur dynamique** :
        - Formulaire de connexion avec validation et message de bienvenue.

5. **Tests (unitaires et UI)** :
        - Tests avec JUnit pour valider les fonctionnalités principales.
        - Tests UI avec Espresso pour vérifier l'interface utilisateur.
   
---

## Tests
### Tests unitaires avec JUnit

Exemple :
      ```bash
class CalculatorTest {
   @Test
   fun addition_isCorrect() {
              assertEquals(4, 2 + 2)
   }
}

### Tests UI avec Espresso

Exemple de test Espresso pour le formulaire de connexion :
    ```bash
   @Test
   fun button_isDisplayed() {
       onView(withId(R.id.myButton)).check(matches(isDisplayed()))
   }

### Création d’un Scénario de Tests 
- Formulaire de connexion :

     - Entrer le nom d'utilisateur.
      
    - Entrer le mot de passe.
      
    - Cliquer sur « Se connecter ».
      
    - Vérifier l’affichage d’un message de bienvenue.

   ```bash
   @Test
  fun loginForm_isFunctional() {
      val scenario = ActivityScenario.launch(MainActivity::class.java)
      // Saisir le nom d’utilisateur
      onView(withId(R.id.username)).perform(typeText("user"), closeSoftKeyboard())

      // Saisir le mot de passe
      onView(withId(R.id.password)).perform(typeText("password"), closeSoftKeyboard())

      // Cliquer sur le bouton « Se connecter »
      onView(withId(R.id.loginButton)).perform(click())

      // Vérifier que le message de bienvenue est affiché
      onView(withId(R.id.welcomeMessage)).check(matches(isDisplayed()))
  }

---

## Installation et exécution
   1. **Pré-requis* :
        - Android Studio installé (version récente).
        - SDK Android configuré.

   2. **Étapes d'installation* :
        - Importez le projet dans Android Studio.
        - Synchronisez les dépendances Gradle.

   3. **Exécution des tests* :
        - Cliquez avec le bouton droit sur les classes de test et sélectionnez Run Tests.
     
---

## Contributeurs
- Salamata Nourou MBAYE
- Celaire Idriss OKA
- Chaimae MOUHDA


