# Java 

## E-Learning 

Implementiere eine E-Learning Plattform. Im E-Learning System soll es einige Klassen geben: 
Ein `Student` hat eine Identifikationsnummer, einen Namen und besucht verschiedene `Lectures`(Vorlesungen). 
In einer `Lecture` bekommt ein `Student` eine Reihe von `Assignments`. 
Ein `Assignment` kann mit einer `int grade(double points)` Methode bewertet werden - Achtun beim erstellen eines Assignments
wird die erreichte Punktezahl noch nicht gesetzt, sondern erst beim Aufruf der `grade` Methode.

Wir brauchen also zumindest folgende Klassen: 
* Student: name, matrikelnummer, zugeordnete lectures
* Lecture: name, zugeordnete assignments
* Assignment: name, maximale Punktezahl, erreichte Punktezahl
* Main

Neben getter, setter & Konstruktor werden folgende Methoden benötigt:
Student: 
* `void enroll(Lecture lecture)` fügt einem Student eine Lecture zu.
* `void getSchoolReport()` sollte ein Zeugnis auf die Konsole drucken - im Format(`Angewandte Mathematik............ Befriedigend`). 
Lecture:
* `Integer getGrade()` gibt die aus allen bewerteten Assignments für diese Lecture errechnete Durchschnittsnote ab (entscheide selbst ob 3.5 zu einer 3 oder 4 wird ;))
Assignment: 
* `boolean isGraded()` gibt an ob ein Assignment bereits bewertet wurde oder nicht
* `int grade(double points)` bewertet ein Assignment mit der angebeben Punktezahl. 
Schema zum Umrechnen: 
Entsprechen die erreichten Punkte 0-50% der maximal erreichbaren Punktezahl gibt's eine 5
Für 50-65% gibt es eine 4
Für 65-80% gibt es eine 3
Für 80-90% gibt es eine 2
Für 90-100% gibt es eine 1

Schreibe auch ein paar Testfälle für dein Programm: 
1. Teste die `int grade(double points)` Methode Ausführlich mit verschiedenen Assignments mit unterschiedlichen maximal erreichbaren Punktezahlen. Pro Note mindestens ein Testfall. 
2. Teste die `Integer getGrade()` Methode der lecture ausführlich. Gibt es noch keine bewerteten Assignments soll die Methode `null` zurück liefern

Erstelle dir außerdem in der Main Klasse ein paar Schüler mit einigen Lectures und drucke ihre School Reports auf die Konsole.