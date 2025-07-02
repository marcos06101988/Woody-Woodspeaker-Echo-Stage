# Woody-Woodspeaker-Echo-Stage

## Projektbeschreibung und Konzept

Die Idee zur Installation entstand durch mein Digezz-Projekt „Woody Woodspeaker“, ein selbst gebauter, analoger Speaker mit nostalgischem Look. Dieser Speaker sollte ins Zentrum einer interaktiven Installation rücken, die im Foyer des Medienhauses der FHGR aufgebaut wurde. Der offene Raum und die bereits vorhandene Bühne eigneten sich ideal für eine interaktive Lichtperformance. Die Grundidee war, BesucherInnen durch ihr eigenes Audiosignal, abgespielt über den Woody-Speaker, zu einem Teil der Installation zu machen: Ihr Sound löst eine Visualisierung aus, die sich in den LatLights visuell widerspiegelt. Solange das Mikrofon im Speaker nicht aktiviert wird, läuft ein Kaltweisslicht-Verlauf über die Lampen im Loop.

Der Impuls für diese Fusion kam beim SaintWhoo Festival im Juni, wo ich bereits mit den LatLights arbeiten durfte. Die Begeisterung für deren Ausdrucksstärke und Wirkung im Raum war so stark, dass ich diese in ein eigenständiges FH-Projekt übertragen wollte. Daraus wurde schrittweise das Konzept einer Echtzeit-Musikvisualisierung mit TouchDesigner.


## Umsetzung
Die Umsetzung erfolgte mit TouchDesigner und einer Reihe von Audio- und visuellen Operatoren. Das Projekt wurde in mehrere Bereiche aufgeteilt:


### Audioanalyse mit audioAnalysis!

Das Audiosignal wird live vom Mikrofon erfasst und analysiert, um Pegelveränderungen (Bass etc.) zu extrahieren. Diese steuern die Trigger.


### Zwei Animationsebenen (RGB / CWWW)
Je nach Logik entscheidet ein switch_animationen, ob RGB- oder CWWW-Visualisierung aktiv ist. Wenn das Mikro nicht aktiviert ist und keine Musik abgespielt wird, läuft im Loop ein Kaltweisslicht-Verlauf über alle Lampen. 


### Output zu den LatLights
Die finale Visualisierung wird über ein select_TOP und ein switch_TOP an den LatLights-Controller weitergegeben.

Alle Module sind beschriftet und annotiert – wie z.b. auch der switch_animationen-Knoten, der die Annotation „Animations-Auswahl“ trägt mit der Beschreibung „Schaltet zwischen RGB- und CWWWbasierend auf Logik-Trigger“


![WhatsApp Image 2025-07-02 at 09 49 16 (1)](https://github.com/user-attachments/assets/f6af7326-c87d-4791-ac2d-dd386492a554)
