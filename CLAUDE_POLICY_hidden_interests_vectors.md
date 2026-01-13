# Policy: Hidden Interests Vector Analysis

## Kada naudoti

Naudok šią metodiką kai vartotojas:
- Nori suprasti kodėl organizacijoje/situacijoje yra konfliktas
- Klausia apie "tikrus motyvus" vs oficialias pozicijas
- Nori vizualizuoti stakeholder interesus
- Mini "principal-agent", "collective action", arba panašias problemas
- Prašo analizuoti kodėl "visi žino, bet niekas nedaro"

## Metodika: Two-Pass Interest Analysis

### PASS 1: Identifikuok dalyvius ir sluoksnius

Kiekvienam dalyviui (stakeholder) apibrėžk:

```
DALYVIS: [Pavadinimas]
├── 🔒 PASLĖPTA (hidden layer):
│   └── Tikri motyvai, kurių viešai nepripažįsta
│   └── Asmeniniai interesai (bonusai, karjera, baimės)
│   └── Struktūriniai interesai (pozicijos išsaugojimas)
│
├── 👁 MATOMA (observable layer):
│   └── Oficialūs pareiškimai
│   └── Stebimas elgesys
│   └── Viešos pozicijos
│
└── 📐 VEKTORIUS (3D erdvėje):
    └── X: Pelnas/ekonominė nauda →
    └── Y: Valdžia/kontrolė ↑
    └── Z: Augimas/ekspansija ↗
```

### PASS 2: Analizuok sąveikas

1. **Vektorių suma** = ELGESYS (tai ką matome)
   - Niekas individualiai nesiekė šio rezultato
   - Emergentinis fenomenas

2. **Kibernetikos principas**:
   - Sistemos dalis mato ją ribotai (per savo poziciją)
   - Nėra "objektyvaus stebėtojo iš šalies"
   - Kiekvienas optimizuoja savo vietą = racionalu jam

3. **Olson'o dilema**:
   - Individualiai optimalūs veiksmai → kolektyviai blogas rezultatas
   - Pakeisti sistemą = pralaimėti individualiai

### PASS 3: Sprendimo dizainas (Two-Pass metodas)

**Pass 1 - Transliacijos → Skaidrumas:**
- Paslėptus interesus paversti legitimiais
- Ne "demaskuoti", o normalizuoti
- Formatas: "[Dalyvis]: Norime [tikras interesas]" → OK, tai normalu

**Pass 2 - Transformacijos → Win-Win:**
- Surasti mechanizmus kur A interesai patenkinami per B interesus
- Ne kompromisas, o dizainas
- Formatas: [A duoda] ↔ [B gauna]: [Mechanizmas]

## Vizualizacijos šablonas

Kai vartotojas prašo vizualizacijos, sukurk HTML su:

1. **3D erdvė (Three.js)**:
   - Vektoriai iš centro (paslėpti = punktyriniai, 50% opacity)
   - Suma = ELGESYS (solidus, ryškus)
   - Interaktyvu (mouse drag rotation)

2. **WHAT-IF mygtukas**:
   - Perjungia tarp "paslėptų" ir "skaidrių" vektorių
   - Skaidrūs = suartėja (mažesnė įtampa)
   - Vizualiai parodo skaidrumo naudą

3. **Legendos panelė**:
   - Kiekvienas dalyvis su spalva
   - 🔒 Paslėpta vs 👁 Elgesys

4. **PESTEL sekcija** (jei aktualu):
   - Išorinės jėgos veikiančios visus dalyvius

5. **Transformacijų matrica**:
   - Lentelė: A duoda → B gauna | Mechanizmas

## Kalbos pasirinkimas

- Jei vartotojas rašo lietuviškai → visas output lietuviškai
- Jei angliškai → angliškai
- Vizualizacijos UI kalba = vartotojo kalba

## Tikslios formuluotės (SVARBU)

❌ NETEISINGA: "Sistemos dalis negali matyti visos sistemos"
✅ TEISINGA: "Sistemos dalis mato ją ribotai – per savo poziciją"

❌ NETEISINGA: "Interesai nesuderinami"  
✅ TEISINGA: "Tarp interesų egzistuoja nuolatinė įtampa"

❌ NETEISINGA: "Problema neišsprendžiama"
✅ TEISINGA: "Sprendimas reikalauja dizaino, ne kompromiso"

## Pavyzdinis workflow

```
Vartotojas: "Paaiškink konfliktą tarp X ir Y"

1. Identifikuok dalyvius (ne tik X ir Y - kas dar įtrauktas?)
2. Kiekvienam: paslėpta vs matoma
3. Apibrėžk vektorius 3D erdvėje
4. Apskaičiuok sumą (emergentinis elgesys)
5. Paaiškink kodėl problema išlieka (kibernetika + Olson)
6. Pasiūlyk Two-Pass sprendimą
7. Jei prašo - sukurk vizualizaciją
```

## Šaltiniai (cituoti kai aktualu)

- Olson, M. (1965). The Logic of Collective Action
- von Foerster, H. - Second-order cybernetics
- Ashby, W.R. - Law of Requisite Variety
- Liebman & Mahoney (2017) - Year-end budget spending research

## Failų struktūra vizualizacijai

```
[projektas]/
├── index.html          # Pagrindinis failas (GitHub Pages)
├── [pavadinimas].html  # Alternatyvus pavadinimas
└── CLAUDE_POLICY_hidden_interests_vectors.md  # Šis failas
```

---

*Ši metodika sukurta analizuojant Mažeikių Nafta (Orlen Lietuva) atvejį. Tinka bet kokiai multi-stakeholder situacijai kur egzistuoja paslėpti vs oficialūs interesai.*
