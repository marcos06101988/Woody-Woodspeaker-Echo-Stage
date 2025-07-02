# Woody Woodspeaker Echo-Stage

## 1. Projektidee und Konzept

Die Idee zur Installation entstand durch mein Digezz-Projekt „Woody Woodspeaker“, ein selbst gebauter, analoger Speaker mit nostalgischem Look. Dieser Speaker sollte ins Zentrum einer interaktiven Installation rücken, die im Foyer des Medienhauses der FHGR aufgebaut wurde. Der offene Raum und die bereits vorhandene Bühne eigneten sich ideal für eine interaktive Lichtperformance. Die Grundidee war, BesucherInnen durch ihr eigenes Audiosignal, abgespielt über den Woody-Speaker, zu einem Teil der Installation zu machen: Ihr Sound löst eine Visualisierung aus, die sich in den LatLights visuell widerspiegelt. Solange das Mikrofon im Speaker nicht aktiviert wird, läuft ein Kaltweisslicht-Verlauf über die Lampen im Loop.

Der Impuls für diese Fusion kam beim SaintWhoo Festival im Juni, wo ich bereits mit den LatLights arbeiten durfte. Die Begeisterung für deren Ausdrucksstärke und Wirkung im Raum war so stark, dass ich diese in ein eigenständiges FH-Projekt übertragen wollte. Daraus wurde schrittweise das Konzept einer Echtzeit-Musikvisualisierung mit TouchDesigner.
<br>
<br>
## 2. Umsetzung
Die Umsetzung erfolgte mit TouchDesigner und einer Reihe von Audio- und visuellen Operatoren. Das Projekt wurde in mehrere Bereiche aufgeteilt:


### >>> Audioanalyse mit audioAnalyze!
- Das Audiosignal wird live vom Mikrofon erfasst und analysiert, um Pegelveränderungen zu extrahieren
- Diese steuern die Trigger


### >>> Zwei Animationsebenen (RGB / KW)
- Je nach Logik entscheidet ein switch_animationen, ob RGB- oder CWWW-Visualisierung aktiv ist 
- Wenn das Mikro nicht aktiviert ist und keine Musik abgespielt wird, läuft ein Kaltweisslicht-Verlauf


### >>> Output zu den LatLights
- Die Visualisierung wird über ein select_TOP und ein switch_TOP an die LatLights weitergegeben.


Alle Module sind beschriftet und annotiert – wie z.b. auch der switch_animationen-Knoten, der die Annotation „Animations-Auswahl“ trägt mit der Beschreibung „Schaltet zwischen RGB- und CWWWbasierend auf Logik-Trigger“
<br>
<br>
## 3. Komponentenplan

Die Installation besteht aus:

### **Technik**
- LatLights (RGBW LED-Röhren mit DMX-Controller)
- Woody Woodspeaker als Audioquelle
- Mikrofon / Audiointerface zur Live-Erfassung
- TouchDesigner-Laptop als Steuerzentrale

### **Aufbau**
- Traversenrahmen und Stangen
- Holz-Bühne
<br>

## 4. Umsetzungsprozess

### Startpunkt

Erste Experimente mit TouchDesigner und einem simplen RGB-Shader. Rasch wurde klar, dass ich ein Umschalten zwischen mehreren Animationsebenen (RGB/CWWW) brauche.

### Rückschläge

- *Überkomplexität* <br>
Die Idee, auch die Kamera für Personenerkennung zu nutzen, wurde zu aufwändig in Kombination mit Musikvisualisierung. Die Überlegung war, dass sich die Visualisierung auch verändert durch das Betreten der Bühne. Ich habe diesen Teil auch gestrichen um Stabilität im Projekt zu gewährleisten. Lieber weniger aber dafür funktioniert alles ordentlich war so mein Fazit daraus.

- *Performanceprobleme* <br>
Einige Rampen-Animationen liefen zu langsam. Die transform-TOPs wurden daher skaliert (z. B. auf 0.4), um Realtime-Tauglichkeit zu erhalten.

- *Unklare Logik* <br>
Die Verschaltung des Audio-Triggers mit dem switch_animationen-TOP war nicht einfach für mich. Ich habe hier mehrfach umgebaut und Feedback von Jan und ChatGPT einholen müssen bis es wirklich funktionierte.

### Hilfequellen
Wenn ich nicht weiterkam, habe ich ChatGPT verwendet – besonders bei der Erklärung von select_TOP und Triggerlogiken. Zusätzlich haben mir YouTube-Tutorials zu Musikvisualisierung geholfen. Und natürlich hat mir Jan, hilfsbereit wie er ist, unter die Arme gegriffen wenn ich irgendwo angeschlagen bin und auch mit KI nicht weiterkam.

### Der finale Tag
Die letzten 24 Stunden vor der Abgabe waren intensiv. Doch schlussendlich hat alles funktioniert – die Lichter reagierten korrekt auf die Musik. Ein wohlverdientes Calanda Glatsch auf der Bühne :) <br>
<br>
<br>
![WhatsApp Image 2025-07-02 at 09 55 32](https://github.com/user-attachments/assets/6980a7f2-d800-4f9c-9106-2a371550cac9)
<br>
<br>
## 5. Selbstreflexion und Lernforschritt

Ich habe in diesem Projekt nicht nur gelernt, wie TouchDesigner im Detail funktioniert, sondern auch, wie wichtig Modularität und klare Logik beim Aufbau sind. Komplexität muss reduziert werden, um in der Zeit, die vorhanden war etwas zu zeigen, das funktioniert. Besonders beeindruckt hat mich, wie stark KI (z. B. ChatGPT) und Tutorials den Fortschritt beschleunigen – aber nur in Kombination mit eigenem Ausprobieren und Testen!

Ich habe gelernt, Projekte besser zu planen, Flexibilität einzuplanen und auch Rückschläge sportlich zu nehmen. Die Bandbreite von CreaTec ist beeindruckend – und ich freue mich darauf, weitere Bereiche auszuprobieren. Dieses Projekt hat mich begeistert – und manchmal auch an meine Grenzen gebracht. Vorrallem werde ich die Funktion mit der Kamera und der Bewegungserkennung auf der Bühne mit eigener Visualisierung definitiv noch umsetzten in den nächsten Tagen. Es war vielleicht zuerst etwas zu ambitioniert aber ich denke mit dem Wissen und dem Fortschritt den ich gemacht habe in TouchDesigner sollte ich das auch hinkriegen. Damit ich für die Zukunft auch verstehe wie das mehreren Layern funktioniert. Jedoch bin ich mit dem Ergebniss sehr zufrieden und hoffe es gefällt den BesucherInnen genauso.


Die Umsetzung meines Lichtinstallations-Konzepts mit TouchDesigner, Audioinput und LatLights war eine kreative Herausforderung. Es hat mir riesigen Spass gemacht, alle Komponenten zu verbinden und die Bühne im Medienhaus mit Leben zu füllen. Die Reaktionen der BesucherInnen bis jetzt haben gezeigt, dass sich die Mühe gelohnt hat. Am Ende blieb nur noch eins zu sagen: Installation funktioniert und Ziel erreicht – Calanda verdient würd ich mal sagen!

## 6. Screenshots Projetkstruktur
### Projektübersicht
![Projektübersicht](https://github.com/user-attachments/assets/f13b554b-5bbe-42b7-b612-e907fdeed4c1)

### Coldwhite Animation
![Coldwhite Animation](https://github.com/user-attachments/assets/6da548b4-9f75-4c9d-89f2-2526bf090db3)

### RGB Animation bei Interaktion
![RGB Animation bei Interaktion](https://github.com/user-attachments/assets/736a2430-bda6-43d5-b5e4-db729807e1e9)

