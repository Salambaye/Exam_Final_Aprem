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


---

## Instructions pour exécuter le projet

1. **Cloner le projet** :
   ```bash
   git clone https://github.com/username/exam-final-android.git
   cd exam-final-android

2. Ouvrir le projet dans Android Studio :
      ```bash
   Sélectionnez le fichier build.gradle dans le répertoire racine.

4. Exécuter l'application :
      ```bash
        Connectez un appareil ou démarrez un émulateur Android.
        Cliquez sur Run > Run 'app' ou utilisez le raccourci Shift + F10.

Captures d'écran
Débogage avec Logcat :

Gestion des exceptions :

Interface utilisateur :

Tests réussis :

Note : Remplacez path/to/... par les chemins des captures d'écran dans votre projet.
Fonctionnalités

    Débogage avec Logcat :
        Ajout de journaux (logs) pour suivre le comportement de l'application.
        Exemple :
   ```bash
        Log.d("MainActivity", "Application démarrée")

    Gestion des exceptions courantes :
        Gestion des exceptions telles que NullPointerException et IndexOutOfBoundsException.
        Utilisation de vérifications avant l'accès aux données.

    Interface utilisateur dynamique :
        Formulaire de connexion avec validation et message de bienvenue.

    Tests (unitaires et UI) :
        Tests avec JUnit pour valider les fonctionnalités principales.
        Tests UI avec Espresso pour vérifier l'interface utilisateur.

Tests
Tests unitaires

Exemple :
   ```bash
@Test
fun addition_isCorrect() {
    assertEquals(4, 2 + 2)
}

Tests UI

Exemple de test Espresso pour le formulaire de connexion :

   ```bash
@Test
fun loginForm_isFunctional() {
    onView(withId(R.id.username)).perform(typeText("user"), closeSoftKeyboard())
    onView(withId(R.id.password)).perform(typeText("password"), closeSoftKeyboard())
    onView(withId(R.id.loginButton)).perform(click())
    onView(withId(R.id.welcomeMessage)).check(matches(isDisplayed()))
}

Installation et exécution

    Pré-requis :
        Android Studio installé (version récente).
        SDK Android configuré.

    Étapes d'installation :
        Importez le projet dans Android Studio.
        Synchronisez les dépendances Gradle.

    Exécution des tests :
        Cliquez avec le bouton droit sur les classes de test et sélectionnez Run Tests.
