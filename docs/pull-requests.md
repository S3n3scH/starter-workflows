# Pull‑Anfragen

Vorschlagen, Überprüfen und Zusammenführen von Codeänderungen mithilfe von Pull‑Anfragen, um effektiv zusammenzuarbeiten und die Codequalität aufrechtzuerhalten.

Pull‑Anfragen sind Vorschläge zum Zusammenführen von Codeänderungen in einem Projekt. Eine Pull‑Anfrage ist GitHubs wichtigstes Feature für die Zusammenarbeit: Sie ermöglicht es, Änderungen zu besprechen und zu überprüfen, bevor sie zusammengeführt werden. Dadurch können Teams Probleme frühzeitig erkennen und die Codequalität beibehalten.

[Anzeigen Ihrer Pull‑Anfragen](https://github.com/pulls?ref_product=github&ref_type=engagement&ref_style=button)

## Umgang mit Pull‑Anfragen

Eine Pull‑Anfrage vereint den Kontext, den Prüfer benötigen, um eine Änderung zu verstehen. Dieser Kontext ist in Registerkarten unterteilt:

- Die Registerkarte **Konversation** enthält die Beschreibung, die Zeitleiste, Kommentare und Bewertungen.
- Auf der Registerkarte **Commits** wird gezeigt, wie sich die Pull‑Request‑Verzweigung im Laufe der Zeit geändert hat.
- Auf der Registerkarte **Prüfungen** werden automatisierte Tests, Builds und andere Überprüfungen angezeigt.
- Der Tab **Geänderte Dateien** zeigt das Diff, das Prüfer verwenden, um die vorgeschlagenen Änderungen nachzuvollziehen.
- Auf der Registerkarte **Ergebnisse** werden die Ergebnisse der automatisierten Codeüberprüfung angezeigt, z. B. Warnungen und Hinweise für die vorgeschlagenen Änderungen.

Getrennt von den Registerkarten hebt der **Zusammenführungsstatus** Blocker, fehlende Genehmigungen und andere Anforderungen vor dem Zusammenführen hervor. Er wird im Header der Pull‑Anfrage und im Merge‑Feld angezeigt.

Zusammen helfen diese Ansichten Autor:innen und Prüfer:innen dabei, die Änderung zu diskutieren, Rückmeldungen nachzuverfolgen und zu entscheiden, wann die Pull‑Anfrage bereit zum Zusammenführen ist.

## Entwürfe von Pull‑Anfragen

Beim Erstellen einer Pull‑Anfrage können Sie diese als Entwurf kennzeichnen. Entwurfs‑Pull‑Anfragen können nicht zusammengeführt werden, und Code‑Owner werden nicht automatisch zur Überprüfung aufgefordert. Entwürfe sind nützlich, wenn Sie Fortschritte teilen möchten, ohne formell Reviews anzufordern.

Wenn Sie bereit sind, Feedback zu erhalten, können Sie Ihren Entwurf als „zur Überprüfung bereit“ markieren. Dann werden Reviews von allen relevanten Code‑Ownern angefordert. Eine Pull‑Anfrage kann jederzeit in einen Entwurf zurückkonvertiert werden. Siehe: [Die Phase eines Pull Requests ändern](/de/pull-requests/how-tos/create-pull-requests/changing-the-stage-of-a-pull-request).

## Pull‑Request‑Referenzen und Zusammenführen von Branches

Wenn Sie einen Pull‑Request öffnen, erstellt GitHub temporäre Git‑Refs, die auf den Head‑Branch der Pull‑Anfrage und, wenn möglich, auf ein simuliertes Merge‑Ergebnis verweisen. Diese Refs helfen GitHub und Integrationen dabei, den Pull‑Request zu evaluieren, ohne den Basis‑Branch zu verändern.

Für die meisten Mitwirkenden bleiben diese Refs unsichtbar. Sie sind relevant, wenn Sie Automatisierung schreiben, CI‑Verhalten debuggen oder den Pull‑Request‑Status lokal abfragen möchten. Informationen zur Verwendung des GitHub Actions Merge‑Branch finden Sie unter: [Ereignisse zum Auslösen von Workflows](/de/actions/reference/workflows-and-actions/events-that-trigger-workflows#how-the-merge-branch-affects-your-workflow).

## Unterschiede zwischen Vergleichsseiten und Pull‑Request‑Seiten

Vergleichsseiten und Pull‑Request‑Seiten können geänderte Dateien auf Grundlage unterschiedlicher Merge‑Basen berechnen. Daher können dieselben Branches an verschiedenen Orten unterschiedliche Diffs anzeigen.

Das ist besonders dann wichtig, wenn sich der Basis‑Branch seit der Erstellung der Pull‑Anfrage geändert hat. Pull‑Request‑Seiten konzentrieren sich darauf, welche Änderungen die Pull‑Anfrage einbringt, während Vergleichsseiten den aktuellen Vergleich zwischen zwei Referenzen zeigen.

## Modelle der kollaborativen Entwicklung

Die Art und Weise, wie Sie Pull‑Anfragen nutzen, hängt vom Entwicklungsmodell Ihres Projekts ab. Gängige Modelle sind das Fork‑and‑Pull‑Modell und das Modell mit gemeinsamem Repository.

### Fork‑and‑Pull‑Modell

Im Fork‑and‑Pull‑Modell kann jeder ein vorhandenes (Upstream‑)Repository forken, wenn der Upstream‑Besitzer das erlaubt. Ein Fork und sein Upstream‑Repository verwenden dieselben Git‑Daten; Inhalte eines Forks sind somit auch vom Upstream und anderen Forks aus zugänglich.

Sie benötigen keine Rechte am Upstream‑Repository, um in Ihren Fork zu pushen. Optional können Sie erlauben, dass Personen mit Push‑Rechten am Upstream Änderungen an Ihrem Pull‑Request‑Branch vornehmen. Dieses Modell ist bei Open‑Source‑Projekten beliebt, da es neuen Mitwirkenden die Teilnahme erleichtert.

> **Tipp:** Mehr Informationen zu Open Source und zum Aufbau einer Community finden Sie in den [Open Source Guides](https://opensource.guide/). Außerdem gibt es kostenlose Kurse bei [GitHub Skills](https://skills.github.com/).

### Modell mit gemeinsamem Repository

Im Modell mit gemeinsamem Repository haben Mitarbeiter:innen Push‑Zugriff auf ein zentrales Repository und erstellen Feature‑Branches für ihre Änderungen. Pull‑Anfragen sind hier nützlich, um Codeüberprüfungen und Diskussionen zu führen, bevor Änderungen in den Hauptbranch integriert werden. Dieses Modell ist häufig bei kleinen Teams und privaten Projekten.

## Weiterführende Lektüre

- [Erstellen eines Pull Requests](/de/pull-requests/how-tos/create-pull-requests/creating-a-pull-request)  
- [Branches](/de/pull-requests/reference/branches)  
- [Einen Pull Request kommentieren](/de/pull-requests/how-tos/review-pull-requests/commenting-on-a-pull-request)  
- [Einen Pull Request von einem Fork erstellen](/de/pull-requests/how-tos/create-pull-requests/creating-a-pull-request-from-a-fork)  
- [Änderungen an einem Pull‑Request‑Branch zulassen, der von einem Fork erstellt wurde](/de/pull-requests/how-tos/work-with-forks/allowing-changes-to-a-pull-request-branch-created-from-a-fork)
