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

**Histogramm-Analyse**

Histogramm und Median zeigen, dass sich die Gesamtbewertung leicht links-schief mit Schwerpunkt 60 – 75 Punkten verteilt.

# Teilauftrag 3

Für die Prognose des Feldes **overall_rating** wurde ein Random-Forest-Regressor mit sieben numerischen Merkmalen trainiert. Eine 5-fach-Cross-Validation ergab einen mittleren MAE von **1,05 Punkten** (± 0,01) und einen mittleren R²-Wert von **0,931** (± 0,001). Das Modell sagt die Gesamtbewertung somit im Schnitt bis auf etwa einen Punkt genau voraus und erklärt über 93 % der Varianz – bei sehr geringer Streuung zwischen den Folds. Die Stichproben-Tabelle bestätigt diese Güte: Vorhersagen und Ist-Werte liegen fast deckungsgleich, Ausreisser bleiben selten. Damit erfüllt das Modell die Qualitäts­anforderungen deutlich.

**Feature-Skalierung:**

Da der Random-Forest baumbasiert arbeitet, ist keine Feature-Skalierung erforderlich..(2.4, aber in Teilauftrag 2 eingefügt, da es 2.4 ist)
