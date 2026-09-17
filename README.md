# IEEE-Smart-Village-Student-Paper-Competition-2026
## When the Lights Go Out: A Hydrogen-Battery Hybrid Microgrid as a Lifeline for Rural Africa

> A computational study investigating whether hydrogen-battery hybrid microgrids can improve the resilience of critical rural infrastructure during multi-day solar energy deficits, using a representative rural healthcare facility in Limpopo, South Africa as a case study.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Electrical Engineering](https://img.shields.io/badge/Electrical-Engineering-orange)
![Energy Systems](https://img.shields.io/badge/Energy-Systems-green)
![Green Hydrogen](https://img.shields.io/badge/Green-Hydrogen-lightgrey)
![Hybrid Microgrid](https://img.shields.io/badge/Hybrid-Microgrid-yellow)
![Energy Storage](https://img.shields.io/badge/Energy-Storage-purple)
![IEEE](https://img.shields.io/badge/IEEE-Student%20Research-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## Author

**Thato Maelane**

Electrical Engineering
Tshwane University of Technology
Pretoria, Gauteng, South Africa

---

## Research Paper

**When the Lights Go Out: A Hydrogen-Battery Hybrid Microgrid as a Lifeline for Rural Africa**

This paper was developed and submitted for the:

**IEEE Smart Village (ISV) Student Paper Competition 2026**

under the theme:

> **Accelerating Resilient Energy Systems & Industrial Decarbonization through Innovation**

This was my **first research paper as a student**.

---

## Project Overview

This research investigates how hydrogen-battery hybrid microgrids could improve the resilience of critical rural infrastructure during prolonged periods of low solar generation.

The study uses a representative rural healthcare and community service cluster in **Limpopo, South Africa**, consisting of:

- A rural healthcare clinic
- Vaccine cold-chain refrigeration
- Medical equipment
- Emergency lighting
- Communications
- A community water pumping station

The research compares two energy-system configurations:

### System A
**Solar PV + Lithium-Ion Battery Energy Storage**

### System B
**Solar PV + Battery Energy Storage + Hydrogen Electrolyzer + Hydrogen Storage + PEM Fuel Cell**

The central engineering concept is that batteries and hydrogen can perform complementary storage functions. Batteries provide efficient short-duration energy storage, while hydrogen can provide longer-duration energy storage during multi-day renewable-energy deficits.

---

## Research Question

> **Can hydrogen storage prevent a rural healthcare facility from losing critical electricity during a multi-day period of severely reduced solar generation?**

The research investigates this question through:

- Computational energy-system modelling
- 96-hour simulation
- Battery storage modelling
- Hydrogen production modelling
- Fuel-cell modelling
- Reliability analysis
- Loss of Power Supply Probability analysis
- Unserved-energy analysis
- Techno-economic analysis
- DC-bus transient analysis
- Community-impact analysis

---

## Problem Statement

Rural communities depend on reliable electricity for services that directly affect people's lives.

For a rural healthcare facility, prolonged electricity interruptions can affect:

- Vaccine refrigeration
- Medical equipment
- Emergency lighting
- Communications
- Water pumping
- Pharmaceutical storage
- Patient services

Solar PV and battery energy storage can provide reliable electricity during normal operating conditions. However, prolonged periods of low solar generation can exhaust battery reserves.

This research investigates whether hydrogen can provide an additional long-duration energy reserve capable of bridging multi-day renewable-energy deficits.

---

## Research Objectives

The study aims to:

- Investigate the resilience of rural critical infrastructure during prolonged solar-energy deficits.
- Compare a battery-only microgrid with a hydrogen-battery hybrid microgrid.
- Quantify energy reliability using Loss of Power Supply Probability (LPSP).
- Calculate unserved electrical energy.
- Evaluate hydrogen storage behaviour during a simulated winter anomaly.
- Compare the lifecycle economics of both configurations.
- Analyse the round-trip efficiency of hydrogen storage.
- Investigate DC-bus voltage behaviour during critical source transitions.
- Examine the potential community benefits of resilient energy infrastructure.
- Connect energy resilience with healthcare, water security and agricultural resilience.

---

## Case Study

The research models a representative rural service cluster in **Limpopo, South Africa**.

The simulated community infrastructure consists of:

- Rural healthcare clinic
- Vaccine cold-chain refrigeration
- Community water pumping station

The electrical demand includes:

| Load | Power |
|---|---:|
| Vaccine refrigeration | 8 kW |
| Lighting and communications | 4 kW |
| Medical equipment | 4 kW |
| Morning patient surge | +6 kW |
| Evening emergency and water-pumping demand | +15 kW |
| **Peak demand** | **37 kW** |
| **Approximate daily energy demand** | **468 kWh** |

---

## System Configurations

### System A — Battery-Only Baseline

The baseline system consists of:

- 150 kWp solar PV
- 400 kWh lithium-ion battery
- No hydrogen storage
- No electrolyzer
- No fuel cell

The battery-only architecture was used as the baseline for comparison.

### System B — Hydrogen-Battery Hybrid

The proposed system consists of:

- 150 kWp solar PV
- 120 kWh lithium-ion battery
- 40 kW PEM electrolyzer
- 100 kg hydrogen storage tank
- 40 kW PEM fuel cell
- 65 kg initial hydrogen reserve

The battery provides short-duration energy balancing while hydrogen provides long-duration energy storage.

---

## Core Engineering Concept

The central concept of this research is:

> **Batteries and hydrogen can serve complementary energy-storage roles.**

**Battery Energy Storage** — suitable for:
- Daily energy shifting
- Fast response
- Short-duration storage
- PV smoothing
- Load balancing

**Hydrogen Energy Storage** — suitable for:
- Multi-day energy storage
- Long-duration backup
- Seasonal energy storage
- Extended renewable-energy deficits

The research therefore does not propose replacing batteries with hydrogen. Instead, it investigates a **hybrid architecture** where both technologies perform different functions.

---

## Energy Management Strategy

The Energy Management System uses a deterministic priority-dispatch strategy.

When:

```
P_PV > P_Load
```

surplus energy is used to:

1. Supply the load
2. Charge the battery
3. Produce hydrogen using the electrolyzer

When:

```
P_PV < P_Load
```

the system:

1. Uses available PV generation
2. Discharges the battery
3. Activates the fuel cell when required

### Hydrogen Production Model

The hydrogen production rate is represented by:

```
m_H2(t) = [P_elec(t) × η_elec × η_compress] / LHV_H2
```

Model parameters:

- Electrolyzer efficiency = 62%
- Compression efficiency = 97%
- Hydrogen LHV = 33.33 kWh/kg

### Fuel Cell Model

The fuel-cell electrical output is represented by:

```
P_FC(t) = m_H2_consumed(t) × η_FC × LHV_H2
```

where:

- Fuel-cell efficiency = 50%

### Hydrogen Round-Trip Efficiency

The hydrogen storage pathway is calculated as:

```
η_RTE = η_elec × η_compress × η_FC
η_RTE = 0.62 × 0.97 × 0.50
η_RTE ≈ 30.1%
```

The research recognises that hydrogen has substantially lower round-trip efficiency than lithium-ion battery storage. The engineering question investigated is therefore not whether hydrogen is more efficient than batteries, but whether hydrogen can provide a longer-duration storage function that batteries alone may not economically provide.

---

## Simulation Scenario

A 96-hour winter solar anomaly was modelled, representing a period of severe solar-energy reduction in the Limpopo winter environment.

| Day | Condition | Solar Factor |
|---|---|---:|
| Day 1 | Clear Conditions | 1.00 |
| Day 2 | Heavy Overcast | 0.13 |
| Day 3 | Sustained Storm | 0.10 |
| Day 4 | Partial Clearing | 0.50 |

The scenario was designed to investigate system behaviour during several consecutive days of severely reduced renewable generation.

---

## Key Simulation Results

| Metric | System A | System B |
|---|---:|---:|
| PV capacity | 150 kWp | 150 kWp |
| Battery capacity | 400 kWh | 120 kWh |
| Hydrogen storage | None | 100 kg |
| Electrolyzer | None | 40 kW |
| Fuel cell | None | 40 kW |
| Hydrogen pre-charge | N/A | 65 kg |
| Blackout hours | 47 | 0 |
| Unserved energy | 727.4 kWh | 0 kWh |
| LPSP | 49.0% | 0.0% |
| Hydrogen round-trip efficiency | N/A | 30.1% |
| 20-year LCOE | $0.272/kWh | $0.155/kWh |

### Main Simulation Finding

**System A — Battery Only**

The battery-only system became depleted during the prolonged solar deficit. The simulation produced:

- Blackout duration = 47 hours
- LPSP = 49.0%
- Unserved energy = 727.4 kWh

**System B — Hydrogen-Battery Hybrid**

The hydrogen-battery hybrid system maintained the simulated critical load throughout the scenario. The simulation produced:

- Blackout duration = 0 hours
- LPSP = 0.0%
- Unserved energy = 0 kWh

The hydrogen reserve allowed the system to continue supplying electricity after the battery reached its minimum state of charge.

---

## Techno-Economic Analysis

The study evaluates both architectures over a 20-year period.

- **System A** — 20-year LCOE = $0.272/kWh
- **System B** — 20-year LCOE = $0.155/kWh

The simulated difference corresponds to approximately **43% lower LCOE** for System B under the assumptions used in the study.

The analysis incorporates battery replacement assumptions and the different assumed lifetimes of the storage technologies.

---

## Power Quality Validation

Energy availability alone is not sufficient for critical healthcare infrastructure. The research therefore includes a separate analytical transient model to investigate DC-bus behaviour during critical source transitions.

**Event 1 — PV Generation Collapse**

The battery converter compensates for the loss of PV generation.

- Nominal voltage = 400 V
- Minimum voltage = 382 V
- Voltage deviation = -4.5%

**Event 2 — Load Surge and Fuel-Cell Engagement**

The simulated load increases from 16 kW → 37 kW while the fuel cell begins supporting the system.

- Minimum voltage = 374 V
- Voltage deviation = -6.5%

The analytical model was used to investigate whether the simulated transitions remained within the voltage tolerance assumed in the study for the relevant medical-equipment application.

---

## Community Impact

The research extends beyond electricity generation and storage. The proposed energy architecture is examined as a potential platform for broader community development.

### Healthcare Resilience

Reliable electricity can support vaccine refrigeration, medical equipment, emergency lighting, sterilization, communications, and pharmaceutical storage. A resilient microgrid can therefore support continuity of essential healthcare services during prolonged electricity interruptions.

### Vaccine Cold-Chain Protection

The vaccine refrigeration load is treated as a critical load in the simulation. The research investigates how long-duration energy storage can help maintain refrigeration during prolonged electricity interruptions. The simulation results indicate that the hydrogen-battery configuration maintains the refrigeration load throughout the modelled 96-hour scenario.

### Clean Water Access

Hydrogen production requires treated water. The research explores the possibility of integrating water-treatment infrastructure with community-scale hydrogen systems. The concept is that appropriately designed infrastructure could potentially support both hydrogen production and additional community water services. This is identified as a potential co-benefit requiring further engineering and feasibility analysis.

### Agricultural Resilience

The research also explores a potential future connection between hydrogen infrastructure and green-ammonia production. The conceptual pathway is:

```
Solar Energy
      ↓
Electrolysis
      ↓
Green Hydrogen
      ↓
Green Ammonia
      ↓
Agricultural Inputs
      ↓
Food Security
```

This is presented as a future research direction rather than a demonstrated output of the current simulation.

---

## Research Contribution

This paper makes three primary contributions.

1. **Energy-System Simulation** — A 96-hour computational energy-balance model comparing PV + BESS against PV + BESS + Hydrogen during a severe simulated winter solar anomaly.
2. **Power-Quality Analysis** — A complementary analytical transient model investigating DC-bus voltage behaviour during critical power-source transitions.
3. **Community Impact Analysis** — An engineering analysis connecting resilient energy infrastructure with healthcare, vaccine cold chains, water security, agricultural resilience, and community development.

---

## Technologies Used

**Programming**
- Python

**Numerical Computing & Data Analysis**
- NumPy
- Pandas

**Scientific Visualisation**
- Matplotlib

**Energy-System Modelling**
- Solar PV modelling
- Battery energy storage modelling
- Hydrogen electrolyzer modelling
- Hydrogen storage modelling
- PEM fuel-cell modelling
- Energy balance simulation
- Energy management modelling

**Power-System Analysis**
- DC-bus modelling
- Transient response analysis
- Source-transition analysis
- Voltage deviation analysis

**Data Source**
- NASA POWER

**Python Libraries**
- numpy
- pandas
- matplotlib

---

## Research Workflow

```
Problem Identification
        ↓
Literature Review
        ↓
Limpopo Energy-System Context
        ↓
Community Load Definition
        ↓
PV Generation Modelling
        ↓
Battery Storage Modelling
        ↓
Hydrogen Storage Modelling
        ↓
Energy Management Strategy
        ↓
96-Hour Simulation
        ↓
Reliability Analysis
        ↓
Techno-Economic Analysis
        ↓
Transient Power-Quality Analysis
        ↓
Community Impact Analysis
        ↓
Limitations
        ↓
Future Research
        ↓
Research Paper
```

---

## Repository Structure

```
hydrogen-battery-rural-microgrid/
│
├── README.md
│
├── paper/
│   └── When_the_Lights_Go_Out.pdf
│
├── src/
│   ├── energy_balance.py
│   ├── hydrogen_model.py
│   ├── battery_model.py
│   ├── transient_model.py
│   └── plotting.py
│
├── data/
│   ├── pv_profile.csv
│   ├── load_profile.csv
│   └── simulation_parameters.csv
│
├── results/
│   ├── simulation_results.csv
│   ├── energy_balance.png
│   ├── battery_soc.png
│   ├── hydrogen_storage.png
│   ├── lpsp_comparison.png
│   ├── lcoe_comparison.png
│   └── transient_response.png
│
├── figures/
│   ├── system_architecture.png
│   ├── simulation_results.png
│   ├── economic_analysis.png
│   └── power_quality.png
│
├── docs/
│   ├── methodology.md
│   ├── assumptions.md
│   └── limitations.md
│
├── requirements.txt
│
└── LICENSE
```

---

## Key Engineering Metrics

The research evaluates:

- Loss of Power Supply Probability (LPSP)
- Unserved Energy
- Battery State of Charge (SoC)
- Hydrogen storage level
- Hydrogen production
- Fuel-cell power output
- Solar PV generation
- Load demand
- Hydrogen round-trip efficiency
- Levelized Cost of Energy (LCOE)
- 20-year lifecycle cost
- DC-bus voltage deviation
- Transient recovery behaviour

---

## Limitations

This study is a computational investigation, not a field deployment. The main limitations include:

- The 96-hour weather scenario is a constructed representative anomaly rather than a reproduction of a specific historical event.
- The load profile is representative rather than based on 12 months of metered data from a specific clinic.
- The hydrogen system has not been physically deployed.
- The transient model is an analytical first-order model rather than a hardware-in-the-loop implementation.
- The economic analysis depends on assumed technology costs and component lifetimes.
- The green-ammonia concept requires additional engineering and economic analysis.
- Site-specific feasibility would require detailed solar, load, water, land, safety and infrastructure data.

Therefore, the reported results should be interpreted as simulation results under the stated assumptions, rather than investment-grade system-sizing results.

---

## Future Research

Future work identified in the paper includes:

- Validation using 12-month metered data from a specific rural clinic.
- Historical weather-event analysis.
- Full MATLAB/Simulink Simscape Electrical implementation.
- Hardware-in-the-loop validation.
- Multi-objective system optimization.
- Optimization targeting LPSP below 1%.
- Detailed hydrogen-storage sizing.
- Detailed water-treatment integration.
- Green-ammonia feasibility analysis.
- Community-scale techno-economic assessment.
- Sensitivity analysis of hydrogen and battery costs.
- Long-term degradation modelling.
- Field deployment and experimental validation.

---

## Research Outcome

The study demonstrates through simulation that a hybrid architecture combining:

```
Solar PV
    +
Battery Energy Storage
    +
Hydrogen Storage
    +
PEM Fuel Cell
```

can provide a potential long-duration resilience mechanism for critical rural infrastructure during multi-day solar-energy deficits.

The research highlights the complementary roles of different energy-storage technologies:

```
Battery   → Short-duration energy storage → Daily energy management
Hydrogen  → Long-duration energy storage  → Multi-day energy resilience
```

---

## IEEE Smart Village Student Paper Competition 2026

- **Conference:** 13th IEEE PES & IAS PowerAfrica Conference (PAC 2026)
- **Competition:** IEEE Smart Village Student Paper Competition
- **Theme:** Accelerating Resilient Energy Systems & Industrial Decarbonization through Innovation
- **Category:** Undergraduate Student
- **Participation:** Individual Paper
- **Outcome:** Paper submitted to the IEEE Smart Village Student Paper Competition 2026

---

## Paper Information

- **Title:** When the Lights Go Out: A Hydrogen-Battery Hybrid Microgrid as a Lifeline for Rural Africa
- **Author:** Thato Maelane
- **Institution:** Tshwane University of Technology
- **Department:** Electrical Engineering
- **Location:** Pretoria, Gauteng, South Africa

---

## Academic Significance

This project represents my first student research paper and an early exploration of the intersection between:

```
Electrical Engineering
        +
Renewable Energy
        +
Energy Storage
        +
Hydrogen Technology
        +
Computational Modelling
        +
Energy Access
        +
Community Development
```

The project reflects my interest in developing engineering solutions that address African energy challenges while connecting technical engineering decisions with real community needs.

---

## Skills Demonstrated

- Electrical Engineering
- Energy Systems Engineering
- Renewable Energy
- Microgrid Design
- Battery Energy Storage
- Hydrogen Energy Systems
- Fuel Cell Systems
- Energy Management
- Numerical Modelling
- Computational Simulation
- Python Programming
- Data Analysis
- Techno-Economic Analysis
- Power Quality Analysis
- Transient Modelling
- Research Methodology
- Literature Review
- Technical Writing
- Engineering Problem Solving
- Sustainability Analysis
- Energy Access Analysis

---

## AI Disclosure

The original competition submission included an AI-use disclosure in accordance with the competition requirements.

AI assistance was used during preparation of the paper for:

- Structuring and debugging Python simulation code.
- Supporting development of the analytical transient model.
- Supporting figure generation.
- Editorial suggestions relating to paper structure and language.

The paper identified the engineering assumptions, problem framing, interpretation of results and conclusions as the author's responsibility.

---

## References

The complete academic references are available in:

`paper/When_the_Lights_Go_Out.pdf`

Key sources used in the study include:

- International Energy Agency (IEA)
- South African Department of Science and Innovation
- NASA POWER
- World Health Organization (WHO)
- IEEE
- International Electrotechnical Commission (IEC)
- South African National Energy Development Institute (SANEDI)
- Africa Green Hydrogen Alliance
- Renewable energy and hydrogen-storage literature

---

## Author

**Thato Maelane**

Electrical Engineering
Tshwane University of Technology
South Africa

---

⭐ If you find this research useful, consider giving the repository a star.
