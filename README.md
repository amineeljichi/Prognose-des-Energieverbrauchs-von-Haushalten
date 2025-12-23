# Prognose des Energieverbrauchs von Haushalten mithilfe von maschinellem Lernen

## Projektübersicht
Dieses Projekt analysiert und prognostiziert den Stromverbrauch von Haushalten anhand minutengenauer Verbrauchsdaten. Durch explorative Datenanalyse (EDA), Feature Engineering und verschiedene Modelle des maschinellen Lernens und Deep Learning zielt das Projekt darauf ab, die **globale Wirkleistung** präzise vorherzusagen und aussagekräftige Energieverbrauchsmuster aufzudecken.

Die Lösung unterstützt ein intelligenteres Energiemanagement im Haushalt, Kostenoptimierung und nachhaltigen Energieverbrauch.

---

## Ziele
- Analyse des Energieverbrauchs von Haushalten im Zeitverlauf
- Identifizierung der wichtigsten Einflussfaktoren auf den Energieverbrauch
- Entwicklung zeitbasierter und verzögerter Merkmale für bessere Prognosen
- Training und Evaluierung mehrerer ML- und DL-Modelle
- Vergleich der Modelle mittels robuster Zeitreihenvalidierung

---

## Datensatzbeschreibung
- **Datensätze:** 2.075.259
- **Merkmale:** 8 (1 Datum/Uhrzeit + 7 numerische)
- **Zeitraum:** Dezember 2006 – November 2010
- **Zielvariable:** Globale Wirkleistung (kW)

---

## Technologien & Tools
- Python
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Scikit-learn
- XGBoost
- TensorFlow / Keras
- Google Colab

---

## Projektablauf

### 1 Datenvorverarbeitung
- Fehlende Werte mit Mittelwert/Median behandelt
- Duplikate und irrelevante Spalten entfernt
- Ausreißer mit statistischen Methoden (IQR/Z-Score) behandelt
- Numerische Merkmale mit MinMaxScaler skaliert
- Zeitliche Reihenfolge beibehalten, um Datenlecks zu vermeiden

---

### 2️ Merkmalsentwicklung
- Lag-Merkmale aus Zeitreihendaten erstellt
- Zeitbasierte Merkmale extrahiert (Stunde, Tag, Monat)
- Gleitende Statistiken hinzugefügt, um das zeitliche Verhalten zu erfassen

---

### 3️ Explorative Datenanalyse (EDA)
- Zeitreihen-Verbrauchstrends
- Stündliche und monatliche Saisonalitätsanalyse
- Verteilungsanalyse von Leistungskennzahlen
- Analyse der Nutzung von Unterzählern
- Korrelationsanalyse mit Heatmaps

---

### 4️ Modelle für maschinelles Lernen
Die folgenden Modelle wurden implementiert und evaluiert mit **TimeSeriesSplit-Kreuzvalidierung**:

| Modell | R² | MAE | RMSE | MAPE (%) |

-------------------|--------|---------|---------|----------|

| Lineare Regression | 0,9994 | 0,0143 | 0,0201 | 2,26 |

| Random Forest | 0,9993 | 0,0149 | 0,0222 | 2,06 |

| XGBoost | 0,9977 | 0,0245 | 0,0410 | 3,21 |

| LSTM | 0,9988 | 0,0220 | 0,0292 | 3,52 |

---

##  Wichtigste Ergebnisse
- Lineare Regression und Random Forest erzielten die beste Gesamtleistung.
- LSTM erfasste effektiv zeitliche Abhängigkeiten und Saisonalität.

Feature Engineering verbesserte die Prognosegenauigkeit signifikant.

Es wurde eine starke Korrelation zwischen globaler Wirkleistung und globaler Intensität festgestellt.

---

##  Zukünftige Verbesserungen
- Integration von Echtzeit-Energieverbrauchsprognosen
- Erweiterung der Datenquellen (Wetter, Belegungsmuster)
- Bereitstellung automatisierter Dashboards für die Überwachung
- Optimierung der Deep-Learning-Architekturen
