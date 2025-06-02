# 🧠 Bröstcancerklassificering med Neuralt Nätverk

Detta projekt bygger ett artificiellt neuralt nätverk (ANN) för att **klassificera tumörer som godartade eller elakartade** baserat på det kända bröstcancerdatasetet från `scikit-learn`.

## 🩺 Syfte

Att utveckla en **pålitlig, datadriven AI-modell** som kan användas för att:
- Förbättra screeningprocessen för bröstcancer
- Stödja beslutsfattande inom vården
- Visa hur maskininlärning kan bidra till **medicinsk och affärsmässig nytta**

---

## 📊 Datasetbeskrivning

- Dataset: `Breast Cancer Wisconsin (Diagnostic)`
- Antal observationer: 569
- Variabler: 30 numeriska mått på tumörer (t.ex. radie, textur, symmetri)
- Målvariabel: `target` – 0 = Malign, 1 = Benign

---

## 📈 Analys och Modellering

### 🔍 Exploratory Data Analysis (EDA)
- Beskrivande statistik för alla variabler
- Visualisering av tumörtypers fördelning
- Korrelationsmatris för att hitta starkt samverkande variabler

### 🧠 Modellering med ANN
- Byggt med `MLPClassifier` från scikit-learn
- Normalisering av data med `StandardScaler`
- Utvärdering med:
  - Klassificeringsrapport
  - Konfusionsmatris
  - Accuracy, precision, recall, f1-score

### 🛠️ Optimering med GridSearchCV
- Testade olika antal dolda lager, regulariseringsstyrkor (`alpha`) och solver-algoritmer
- Vald bästa modell:  
  `{'mlp__alpha': 0.0001, 'mlp__hidden_layer_sizes': (30,), 'mlp__solver': 'adam'}`

- Resultat: **97 % accuracy**

---

## 💼 Affärs- och vårdnytta

✅ **För hälsosektorn**:
- Modellen kan integreras i digitala beslutsstödssystem
- Sparar tid och förbättrar diagnostikens tillförlitlighet

✅ **För företag inom MedTech**:
- Grunden för att utveckla AI-baserade screeningprodukter
- Kan bidra till innovation inom e-hälsa, AI-diagnostik och patientnavigering

---

## ▶️ Så här kör du projektet

1. Klona repot:
```bash
git clone https://github.com/sabrinarybak/breastcancer-classification.git
