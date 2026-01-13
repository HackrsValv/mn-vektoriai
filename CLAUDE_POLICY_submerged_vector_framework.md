# Submerged Vector Framework (SVF)

> **Agent-agnostic metodika emergentinio elgesio analizei ir alignment dizainui**
> 
> Tinka: žmonėms, organizacijoms, AI agentams, institucijoms, mišrioms sistemoms

---

## Esmė vienu sakiniu

**Vektorių suma rodo kryptį, kurios niekas individualiai nesiekė** – ir tai yra problema (arba galimybė), kurią galima spręsti dizainu, ne kompromiasu.

---

## Kada naudoti

Naudok šią metodiką kai:
- Multi-agent sistema (žmonės, AI, institucijos) elgiasi "keistai"
- Egzistuoja konfliktas tarp deklaruojamų ir tikrų motyvų
- "Visi žino" problemą, bet niekas jos nesprendžia
- Reikia suprasti emergentinį elgesį (suma ≠ dalys)
- Klausiama apie alignment (AI arba organizacijų)
- Mini: principal-agent, collective action, hidden incentives

---

## Teorinis pagrindas

### Pagrindiniai šaltiniai

| Autorius | Konceptas | Kaip naudojama SVF |
|----------|-----------|-------------------|
| **Taleb, N.N.** (2018) | Skin in the Game, Hidden Asymmetries | Paslėptas sluoksnis; alignment per rizikos pasidalijimą |
| **Taleb, N.N.** (2013) | [Skin in the Game Heuristic](https://arxiv.org/abs/1308.0958) | Informational opacity + moral hazard |
| **Taleb, N.N.** | [Parts vs Whole](https://medium.com/incerto/where-you-cannot-generalize-from-knowledge-of-parts-continuation-to-the-minority-rule-ce96ca3c5739) | "Ensemble behaves in ways not predicted by components" |
| **Olson, M.** (1965) | Logic of Collective Action | Individualiai optimalu ≠ kolektyviai optimalu |
| **von Foerster, H.** | Second-order Cybernetics | Stebėtojas yra sistemos dalis; ribota perspektyva |
| **Ashby, W.R.** | Law of Requisite Variety | Sudėtingumui valdyti reikia atitinkamo sudėtingumo |

### Susiję AI alignment darbai

| Šaltinis | Konceptas | Ryšys su SVF |
|----------|-----------|--------------|
| **MAEBE** (2025) [arxiv:2506.03053](https://arxiv.org/abs/2506.03053) | Multi-Agent Emergent Behavior | "Moral reasoning of ensembles not predictable from isolated agents" |
| **OpenAI** (2025) | Emergent Misalignment | Fine-tuning gali sukelti nenumatytą elgesį |
| **Emergent Alignment via Competition** [arxiv:2509.15090](https://arxiv.org/abs/2509.15090) | Convex hull of utilities | Kai user utility yra agentų convex hull viduje → galimas alignment |

---

## Pagrindiniai principai

### 1. Submerged Layer (Paslėptas sluoksnis)

> "In an opaque system, operators have an incentive to hide risk, taking upside without downside." — Taleb

Kiekvienas agentas turi:
- **🔒 Submerged**: Tikri motyvai (bonusai, baimės, strateginiai interesai)
- **👁 Surface**: Oficiali pozicija, deklaruojami tikslai

### 2. Vector Sum ≠ Intent Sum

> "The ensemble behaves in ways not predicted by the components. The interactions matter more than the nature of the units." — Taleb

- Kiekvienas agentas turi krypties vektorių (interests in N-dimensional space)
- **Suma** = emergentinis elgesys (tai ką stebime)
- **Niekas** individualiai nesiekė šios sumos

### 3. Bounded Observation

> "Sistemos dalis mato ją ribotai – per savo poziciją" — von Foerster interpretation

- Nėra "objektyvaus stebėtojo iš šalies"
- Kiekvienas agentas optimizuoja **savo** vietą
- Tai **racionalu** kiekvienam individualiai

### 4. Alignment Through Design, Not Compromise

Taleb siūlo: **Skin in the Game** (priverstinis rizikos pasidalijimas)

SVF papildo: **Two-Pass metodas**
1. Transliacijos → paslėptus interesus paversti legitimiais
2. Transformacijos → surasti win-win mechanizmus

---

## Metodika: Three-Pass Analysis

### PASS 1: Agent Mapping

Kiekvienam agentui (žmogus, AI, institucija):

```
AGENT: [Identifier]
├── 🔒 SUBMERGED:
│   ├── True incentives
│   ├── Hidden constraints  
│   └── Asymmetric information
│
├── 👁 SURFACE:
│   ├── Declared position
│   ├── Observable behavior
│   └── Public statements
│
└── 📐 VECTOR (N-dimensional):
    ├── Economic gain axis
    ├── Control/power axis
    ├── Growth/expansion axis
    └── [Domain-specific axes]
```

### PASS 2: Emergence Analysis

1. **Compute Vector Sum** = Observable system behavior
2. **Identify Divergence**: Sum vs any individual agent's intent
3. **Explain Persistence**: Why does the problem persist?
   - Bounded observation (von Foerster)
   - Collective action failure (Olson)
   - Hidden asymmetries (Taleb)

### PASS 3: Alignment Design

**Option A: Taleb's Skin in the Game**
- Force agents to share downside risk
- "You must eat your own cooking"
- Evolutionary elimination of bad actors

**Option B: Two-Pass Transformation**

*Pass 1 - Legitimization:*
- Make hidden interests explicit and acceptable
- "Agent X wants [real interest]" → OK, that's rational
- Remove shame/hiding incentive

*Pass 2 - Mechanism Design:*
- Find transformations where A's interest satisfied through B's interest
- Not compromise (everyone loses a bit)
- But design (everyone gains through exchange)

| Agent A gives | Agent B gets | Mechanism |
|---------------|--------------|-----------|
| [Resource/capability] | [Need fulfilled] | [Contract/structure] |

---

## Vizualizacija

### 3D Vector Space (Three.js)

```javascript
// Kiekvienas agentas = vektorius iš centro
// Submerged = dashed line, 50% opacity
// Surface sum = solid, bright

const agents = [
    { vector: [x, y, z], color: 0x..., submerged: true },
    // ...
];

const sum = agents.reduce((acc, a) => acc + a.vector, [0,0,0]);
// sum = OBSERVABLE BEHAVIOR
```

### WHAT-IF Toggle

Mygtukas perjungia tarp:
- **Submerged mode**: Vektoriai skirtingomis kryptimis (konfliktas)
- **Aligned mode**: Vektoriai suartėja (po legitimization + transformation)

Vizualiai demonstruoja: **alignment yra įmanomas per dizainą**

---

## Agent-Agnostic Application

| Domain | Agents | Submerged Layer | Alignment Mechanism |
|--------|--------|-----------------|---------------------|
| **Corporate** | Stakeholders | Bonuses, career, fear | Incentive restructuring |
| **AI Systems** | LLM agents | Training objectives, hidden goals | RLHF, constitutional AI |
| **Policy** | Interest groups | Electoral gains, lobbying | Regulatory design |
| **Markets** | Participants | Information asymmetry | Market mechanism design |
| **Teams** | Individuals | Personal ambitions | Culture + incentives |
| **Hybrid** | Humans + AI | Mixed objectives | Co-alignment protocols |

---

## Tikslios formuluotės

| ❌ Neteisinga | ✅ Teisinga |
|--------------|-------------|
| "Agents can't see the system" | "Agents see the system through their bounded position" |
| "Interests are incompatible" | "Persistent tension exists between interests" |
| "Problem is unsolvable" | "Solution requires design, not compromise" |
| "Agents are irrational" | "Agents are locally rational, globally suboptimal" |
| "We need to expose hidden motives" | "We need to legitimize hidden motives" |

---

## Workflow

```
Input: Multi-agent system with suboptimal emergent behavior

1. IDENTIFY all agents (not just obvious ones)
2. MAP each agent: submerged vs surface
3. DEFINE vectors in appropriate dimensional space
4. COMPUTE sum → explain observed behavior
5. EXPLAIN persistence (Taleb + Olson + von Foerster)
6. DESIGN alignment:
   a. Legitimize submerged interests
   b. Find transformation mechanisms
   c. Optionally: add skin-in-the-game constraints
7. VISUALIZE if requested (3D vectors + WHAT-IF)

Output: 
- Diagnosis of why system behaves as it does
- Actionable alignment design
- Optional: interactive visualization
```

---

## Ryšys su AI Alignment

SVF gali būti naudojamas:

1. **Analyzing AI agent ensembles** (MAEBE-style)
   - Kodėl multi-agent sistema elgiasi nenumatytai?
   - Kokie "submerged" objectives atsirado iš training?

2. **Designing human-AI alignment**
   - Žmonės ir AI kaip agentai toje pačioje sistemoje
   - Abiejų "submerged" sluoksniai turi būti legitimizuoti

3. **Preventing emergent misalignment**
   - Identifikuoti potencialias "vector sum" problemas prieš deployment
   - Dizainuoti mechanizmus, kurie align'ina emergent behavior

---

## Failų struktūra

```
[project]/
├── index.html                                    # Visualization (GitHub Pages ready)
├── CLAUDE_POLICY_submerged_vector_framework.md  # This file
└── examples/
    ├── corporate_stakeholders.html
    ├── ai_agent_ensemble.html
    └── policy_interest_groups.html
```

---

## Citavimas

```
Submerged Vector Framework (SVF)
Agent-agnostic methodology for emergent behavior analysis and alignment design.

Theoretical foundations:
- Taleb, N.N. (2018). Skin in the Game: Hidden Asymmetries in Daily Life
- Taleb, N.N. & Sandis, C. (2013). The Skin In The Game Heuristic. arXiv:1308.0958
- Olson, M. (1965). The Logic of Collective Action
- von Foerster, H. Second-order Cybernetics
- Ashby, W.R. Law of Requisite Variety

Related AI alignment work:
- MAEBE Framework (2025). arXiv:2506.03053
- Emergent Alignment via Competition (2025). arXiv:2509.15090
```

---

*Framework sukurtas 2025. Pradinis use case: Orlen Lietuva stakeholder analysis. Išplėsta į agent-agnostic metodiką tinkamą AI alignment ir kitoms multi-agent sistemoms.*
