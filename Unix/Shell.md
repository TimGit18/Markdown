# Shell-Progrmmierung

## Aufruf 

Das Shell-Skript beginnt mit einer Steueranweisung, gefolgt von Programm-Instruktionen:

    #!/usr/bin/sh
    # hello.sh
    echo "Hello..."
       
Das Shell-Skript wird ausführbar gemacht mit 

`chmod +x hello.sh`

Anschließend wird es auf der Kommandozeile ausgeführt mit 

`./hello.sh`

## Variablen

Globale Variablen sind vom System gesetzt. Lokale werden im Skript deklariert und initialisiert.

    SHELL_PATH = "$HOME/sh"
    echo "$SHELL_PATH"

Die Anführungsstriche demaskieren Leerzeichen und sind im allgemeinen vorzuziehen. 

Bei der Verwendung von Wildcards muss man vorsichtig sein, sie dürfen nicht demaskiert werden. 

Der folgende Befehl kompiliert alle Java-Klassen im Verzeichnis, das mit der Variablen $SOURCE_CORE_DIR deklariert wurde, schreibt die Ergebnisse inklusive der Paketestruktur in das Verzeichnis, 
das mit der Variablen $SOURCE_PROD_DIR deklariert wurde und benutzt dieses Verzeichnis auch noch als Klassenpfad für die Kompilation.

`javac -encoding utf8 "$SOURCE_CORE_DIR"/*.java -d "$PROJECT_PROD_DIR" -cp "$PROJECT_PROD_DIR"`


