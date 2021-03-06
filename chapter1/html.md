## HTML: strukturieren

In die Einführung \(How the internet works\) haben wir schon mal über HTML geredet. HTML steht für Hyper Text Markup Language. HTML besteht aus sogenantent Tags. Es gibt 3 Typen von Tags:

* &lt;Elementname&gt; : Starttag
* &lt;/Elementname&gt; : Endtag
* &lt;Elementname/&gt; : Leertag

Starttags und Endtags werden immer zusammen verwendet. Der Text zwischen den beiden Tags ist das Element. Das Tag sagt etwas darüber aus wie der Text zwischen dem Start- und Endtag dargestellt werden soll. Manche Tags brauchen keinen text, in diesem Fall benutzt man ein Leertag. Ein Leertag ist eine zusammenziehung eines Start- und Endtags ohne text zwischen den beiden. In der folgenden Tabelle findest du ein paar Beispiele.

| Erklärung | HTML |
| :--- | :--- |
| ordinary paragraph text | `<p>text</p>` |
| your most important heading | `<h1>A heading</h1>` |
| a heading at the next level | `<h2>A sub-heading</h2>` |
| a heading at the next level | `<h3>A sub-sub-heading</h3>`... and so on, up to`<h6>` |
| emphasize your text | `<em>text</em>` |
| strongly emphasize your text | `<strong>text</strong>` |
| go to another line | `<br/>`\(you can't put anything inside br, it's a 'Leertag'\) |
| create a link | `<a href="http://djangogirls.org/">link text</a>` |
| make a list | `<ul><li>first item</li><li>second item</li></ul>` |
| define a section of the page | `<div></div>` |

In einen HTML-text werden verschiedene HTML-tags zur strukturierung und korekte darstellung des textes verwendet. Die Tags können dabei verschachtelt werden. Wenn zum beispiel einen Titel ein Link enthält sieht dies so aus:

```
<h1>Titel mit <a href="http://something.com">Link</a></h1>
```

Jede HTML-Seite hat zudem eine Basisstruktur, die immer gleich ist. Das äusserste Tag-Paar ist immer das &lt;html&gt;...&lt;/html&gt;. Dann gibt es zwei Teile: 'Head' und 'Body'. Im 'Body' kommen die informationen die auf der eigentlichen Seite dargestellt werden. Der 'Head' Teil ist dazu da um Meta-Informationen zu definieren. Zum Beispiel der Titel der Seite, welche CSS Files verwendet werden sollen für das Layout, Keywords für die Suchmachine etc.

Die ganze Basisstruktur sieht also so aus:

```
<html>
    <head>
        ...
    </head>
    <body>
        ...
    </body>
</html>
```

Damit der HTML-Text nicht nur für dem Browser, aber auch für normale Menschen ein bisschen strukturierter aussieht lasst man verschachtelte Tags mittels Leerzeichen ein  rücken.

Damit bist du jetzt in der Lage deine Webseite in index.html ein bisschen besser zu gestalten. Du könntest zum Beispiel einen Text mit einem Titel machen und unten dran eine Liste mit Links zu den Seiten von den anderen in deiner Gruppe. Der Inhalt ist momentan nicht das wichtigste, Hauptsache du spielst ein bisschen mit den HTML Tags herum.

Wenn du, während deinen Text in index.html mit HTML-Tags am schmücken bist, mal schauen möchtest wie es als Webseite aussiehen würde, kannst du die Datei zwischendurch auch immer wieder mit deinen Browser öffnen. \(Vorher speichern nicht vergessen!\)

![](/assets/tutorial_screenshot.png)

Wenn du zufrieden bist mit der Inhalt und Struktur deiner Seite, ist es Zeit sie wieder online zu bringen, sie zu 'deployen'. Dazu gehen wir zurück zum Terminal, das im Idealfall immer noch offen ist.

command-line

```
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

    modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
$ git add --all
$ git commit -m "adding html"
[master 9bfcf50] adding html
 1 file changed, 20 insertions(+), 2 deletions(-)
 rewrite index.html (100%)
$ git push
```

Noch dein Github Username und Passwort eingeben und schon ist die neuste Version deiner Webseite online! Woohoow :D!

