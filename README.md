# KIMB-Skript — Interpreter für einfachen Pseudocode

Interpreter für einen einfachen Pseudocode geschrieben in JavaScript.

>
> Projekt in der Entwicklung
> 

## Über die Sprache

>
> Zieht bald ins Wiki um.
>

- Elementare Operationen: +,-,*, /, %
- Elementare Vergleiche: =, >, <, <=, >=, !=
- Boolsche Operatoren: &, |, !, =>, <=
- Zuweisung: a = b, ( :=, ) int a = b, a += b, a++, a--
- Datentypen: Integer (Float), Bool, Array, Object (Attribut, Wert), String, Function
- Schleifen: for, while, do while
- Verzweigung: if, else if, else
- Funktionendeklaration und  Aufrufe: function name( attr = 'default') { return }, name = function () {}
- OOP: keine Klassen, nur Objekte (Funktionen lassen sich dort reinschreiben)
- include(<file.ks>) Function (nur oben im Programm)

### Syntax
- Blöcke mittels {} oder TAB
- Argumente, Gruppierung (zB mathematische Form): ()
- Indizes, Attribute: [0], [attr name]
- Zeilende: ;, UMBRUCH

### Lexer
#### Vorverarbeitung
- uneindeutige Befehle eindeutig machen, zB: TAB-Block zu {}
- include-Dateien einfach dazukopieren
- Unterscheidung von = im Kontext, Zuweisung vs. Vergleich

#### Lexing
- Eindeutiger 3-Buchstaben Code pro Befehl, Namen in [name], 
- Leerzeichen zwischen "Zeilen", Blöcke durch {}

### Parser
- alle Schleifen zu while-Schleife,
- function name() zu name = function ()
- Implikation zu ! a or b

### Evaluator
- feste Funktion doJS um JavaScript auszuführen (quasi system call)
- Debug-Mode

## Web-Oberfläche
- Eingabefeld
- Code-Beispiele
- Bibilotheken (include)
- Debugger
- Output Terminal
