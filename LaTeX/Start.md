# LaTeX

## Dokumentstruktur

Beispiel-Dokument: hello.tex


    \documentclass{article}

    \begin{document}
    First document. This is a simple example, with no
    extra parameters or packages included.
    \end{document}

## Zyklus

### Erzeugung einer DVI-Datei (Device Independent File Format)

`latex hello.tex`

Das ist das eigentliche latex-Kommando. Es erzeugt die folgenden Dateien

* `hello.aux`
* `hello.log` 
* `hello.dvi`  

### Erzeugung einer PS-Datei (PostScript Format)

`dvips hello.dvi`

Das ist das Kommando, was aus einer DVI-Datei eine PostScript-Datei erzeugt, also

* `hello.ps`  

### Erzeugung einer PDF-Datei (Plain Document Format)

`xelatex hello.tex`

Das ist ein latex-Kommando, was als Output ein PDF-Dokument erzeugt. Es erzeugt die folgenden Dateien

* `hello.aux`
* `hello.log` 
* `hello.pdf`  

## Viewer

### DVI-Viewer

Der Aufruf des DVI-Viewers als Teil des texlive-Pakets lautet:

`xdvi hello.dvi`

### PS-Viewer

Der Aufruf des PS-Viewers ist möglich mit Ghostview (gv)

`gv hello.ps`


### PDF-Viewer

Entweder direkt unter WSL in Windows oder:

`xpdf hello.pdf`

## Unterdrückung der Nummerierung von Überschriften

Statt `\section{Einleitung}` schreibst du einfach: `\section*{Einleitung}`

Das Ergebnis: Die Überschrift „Einleitung“ erscheint ohne Nummerierung. Das funktioniert auch für andere Überschriften:

    \chapter*{Einleitung}       % Kapitel ohne Nummer
    \section*{Einleitung}       % Abschnitt ohne Nummer
    \subsection*{Grundlagen}    % Unterabschnitt ohne Nummer

Wichtig: Mit `\section*{...}` wird die Überschrift standardmäßig auch nicht ins Inhaltsverzeichnis aufgenommen.

Wenn du die Nummerierung unterdrücken, die Überschrift aber trotzdem im Inhaltsverzeichnis anzeigen möchtest, verwende:

    \section*{Einleitung}
    \addcontentsline{toc}{section}{Einleitung}

Damit hast du eine unnummerierte Überschrift, die im Inhaltsverzeichnis erscheint.

## Deutsche Sprachpakete verwenden

Die empfohlene Lösung ist es, ein Sprachpaket zu installieren. Dazu führt man im Terminal diesen Befehl aus:

    sudo apt update
    sudo apt install texlive-lang-german

Das Paket enthält die deutschen Sprachdefinitionen, die babel benötigt.

Anschließen prüft man die LaTeX-Datei und verwendet im Quelldokument latexBeispiel.tex:

    \documentclass{article}
    \usepackage[ngerman]{babel}
    \begin{document}
    ...
    \end{document}

Umlaute und Silbentrennung sollten nun korrekt dargestellt werden. 



    

