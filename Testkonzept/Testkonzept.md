# Testkonzept

SEL ist ein Unternehmen, welches über ein bestehendes und funktionierendes Kundenportal verfügt, welches sich typisch einer modernen Webapplikation ständig verbessert und Updates unterfährt. Da es sich um ein etabliertes Projekt handelt, ist das Testkonzept natürlich auch schon definiert worden. Unser PSE-Team wird exakt dieses Konzept übernehmen, da unser Code schlussendlich in der produktiven Umgebung integriert wird und demzufolge allen Anforderungen von SEL entsprechen soll. Testen ist ein derart wichtiger Bestandteil des SEL Projekts, dass der gesamte Entwicklungsprozess darauf ausgelegt ist.

## Ziele

Ziele des Testen im Projekt PSE SEL sind, allfällige Fehler möglichst früh zu erkennen um den Entwicklungsprozess zu vereinfachen und beschleunigen. Ebenfalls sollen Fehler, welche sich beim Refactoring eingeschlichen haben so möglichst schnell entdecken lassen. Testing soll auch als Dokumentationsinstrument dienen, insbesondere das How-To-Test, welches für jede User Story entworfen und umgesetzt wird – noch bevor mit der Implementierung des eigentlichen Codes losgelegt wird.

## Teststrategie

Die Teststrategie beruht auf TDD (Test Driven Development) zusammen mit automatisierten Tests, welche wichtig sind für das Deployment. 

Für die Dokumentation ist es unumgänglich das How-To-Test für jede User-Story zu evaluieren. Dieses How-To-Test ist schlussendlich so gestaltet, dass ein Laie versteht, wie der Code dieser User Story zu testen ist. Demzufolge ist das How-To-Test sehr informell und pragmatisch gehalten. 

Das How-To-Test wird als aller erstes von einem anderem PSE-Teammitglied eingesehen und analysiert. Diese Analyse dient der Verbesserung der Umsetzung sowie der Vermeidung von Fehlern und Unklarheiten. Im gleichen Schritt wie das How-To-Test geschrieben wird, werden auch Unit-Tests implementiert. Um eine User Story abschliessen zu können, müssen alle hier geschribenen Tests erfüllt sein und alle im How-to-Test definierten Frontend-Tests erfolgreich sein. 

## Testarten

Die programmatischen Tests im folgenden Abschnitt werden alle mit dem Framework Pytest geschrieben. 

- **Unit-Tests** werden primär im Backend durchgeführt. Hierfür soll als erster Schritt jeder User Story definiert werden, was wie getestet werden soll. Grundsätzlich soll mit den Unit Tests sichergestellt werden, dass sich der Code wie definiert verhält. Dementsprechend werden für alle hinzugefügten Modelle und Funktionen Tests geschrieben. Die Tests sollen so umfassend sein, dass die Funktionalität des neu implementierten Codes garantiert werden kann. Alle neu implementieren Requests, welche an das Backend gestellt werden können, sollen in gleicher Art und Weise mithilfe von Unit-Tests abgedeckt werden. Als Testdaten werden entweder vordefinierte der SEL-API oder jeweils pro Tests dynamisch erstellte verwendet werden.
  Für den Code im Frontend werden keine Unit-Tests geschrieben. Die Funktionalität dieses Codes soll mithilfe den Integrationstests kontrolliert werden.  
- **Datenbank-Tests** werden mittels dynamisch erzeugten Testdaten durchgeführt. Diese Tests sind jedoch nicht im Aufgabenbereich unseres Teams.
- Für die **Integrationstests** werden keine spezifische Testfälle definiert, sondern jede User Story wird einerseits in sich geschlossen, andererseits im Gesamtkontext des Kundenportals getestet bevor sie abgeschlossen werde kann. Da SEL einem Test Driven Design folgt, werden die Integrationstests jeder User Story vor Beginn der Implementierung definiert. Diese Tests werden vom Entwickler selber, einem Teammitglied, welches den Code reviewt und schlussendlich auch vom PO durchgeführt, bevor der Code der User Story in der produktiven Umgebung eingebettet wird und weiteren Integrationstests unterzogen wird. Hier wird anhand den im How-to-Test definiertem Vorgehen jedes Akzeptanzkriterium getestet.
- **Installationstests** werden nicht benötigt, da es sich bei SEL um ein existierendes Kundenportal handelt.
- Das **GUI** wird manuell getestet. Während dem Durchführen der Integrationstests soll auch sichergestellt werden, dass sich das GUI wie intendiert verhält.
- SEL folgt dem Prinzip “Do it, do it right, do it fast”. SEL befindet sich laut Aussage des Leiters der Entwicklung des Kundenportals noch in der «Do it right» Phase, weshalb noch keine **Stress-Tests** durchgeführt werden.
- Die Anwender der Software sind die Kunden bei SEL. Es darf davon ausgegangen werden, dass der typische Besucher des Kundenportals ein gewisses Vorwissen bezüglich Webseiten und Apps mit sich bringt. Das Entwicklungs-Team von SEL definiert, wie die im Rahmen vom PSE umgesetzten User Stories umzusetzen sind. Dies bedeutet, dass von unserer Seite keine **Usability-Tests** durchgeführt werden. 