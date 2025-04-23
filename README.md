# JeganTwinLB-259

**Beschreibung des Datensatzes:**

Der Datensatz „Player_Attributes“ enthält umfangreiche Informationen zu den Leistungsmerkmalen von Fußballspielern, die über verschiedene Zeitpunkte hinweg erfasst wurden. Jede Zeile repräsentiert den Zustand eines Spielers an einem bestimmten Datum und umfasst Kennzahlen wie Overall Rating, Potential, Dribbling und Schusskraft. Zur eindeutigen Zuordnung wird die player_api_id verwendet, ergänzt durch das Erhebungsdatum. Die interne id wurde entfernt, da sie für die inhaltliche Analyse keinen Mehrwert bietet.


**Datenschutzaspekte:**

Die Daten stammen aus öffentlich zugänglichen Quellen. Es gibt keine privaten Informationen, die jemanden identifizieren könnten. Man sieht nur sportbezogene Werte, und die Nummern helfen nicht, den Spieler genau zu erkennen. Außerdem steht der Datensatz unter einer offenen Lizenz (z. B. CC BY) und darf nur für akademische und nicht-kommerzielle Zwecke verwendet werden. Dabei muss sichergestellt werden, dass keine persönlichen Daten der Spieler rekonstruierbar sind.


# Teilauftrag 2

**Vohrersage**

Ich entscheide mich dafür, das Feld overall_rating als Zielvariable (Target) zu verwenden. Dieses Feld ist numerisch (Wertebereich meist 0–100) und fasst die verschiedenen Fähigkeiten eines Spielers zusammen. Damit kann ich ein Regressionsmodell trainieren, um den Rating-Wert eines Spielers basierend auf anderen Attributen vorherzusagen. Außerdem ermöglicht mir overall_rating, interessante Fragestellungen zu beantworten – beispielsweise, welche Faktoren den größten Einfluss auf die Gesamtbewertung haben.


**Kurze Begründung, wieso overall_rating ein sinnvolles Datenfeld ist**

Das Feld overall_rating bietet eine zusammenfassende Bewertung der spielerischen Fähigkeiten und wird häufig als wichtigste Kennzahl im Scouting und in der Fußballanalyse angesehen. Es spiegelt mehrere Leistungsfaktoren wider, etwa Technik, Physis und Spielintelligenz, und lässt sich daher gut als Zielvariable in Vorhersagemodellen nutzen. Indem man overall_rating in Abhängigkeit anderer Attribute wie potential, dribbling oder finishing untersucht, können Muster und Zusammenhänge erkannt werden, die für Transferentscheidungen oder Trainingspläne relevant sind.


