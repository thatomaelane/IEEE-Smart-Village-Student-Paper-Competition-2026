# IEEE-Smart-Village-Student-Paper-Competition-2026

## When the Lights Go Out: A Hydrogen-Battery Hybrid Microgrid as a Lifeline for Rural Africa

> A computational study investigating whether hydrogen-battery hybrid microgrids can improve the resilience of critical rural infrastructure during multi-day solar energy deficits, using a representative rural healthcare facility in Limpopo, South Africa as a case study.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Electrical Engineering](https://img.shields.io/badge/Electrical-Engineering-orange)
![Energy Systems](https://img.shields.io/badge/Energy-Systems-green)
![Hydrogen](https://img.shields.io/badge/Green-Hydrogen-lightgrey)
![Microgrid](https://img.shields.io/badge/Hybrid-Microgrid-yellow)
![Energy Storage](https://img.shields.io/badge/Energy-Storage-purple)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

# Author

## Thato Maelane

Electrical Engineering  
Tshwane University of Technology  
Pretoria, Gauteng, South Africa

---

# About This Research

This paper was developed for the:

**IEEE Smart Village (ISV) Student Paper Competition 2026**

under the theme:

> **Accelerating Resilient Energy Systems & Industrial Decarbonization through Innovation**

This was my **first research paper as a student**.

The research explores how resilient energy systems can support underserved communities by ensuring that critical infrastructure remains operational during prolonged renewable-energy shortages.

The study focuses specifically on a representative rural healthcare and community service cluster in Limpopo, South Africa.

---

# Research Question

The central question of this research is:

> **Can hydrogen storage prevent a rural healthcare facility from losing critical electricity during a multi-day period of severely reduced solar generation?**

The research compares two energy-system configurations:

### System A
**Solar PV + Lithium-Ion Battery Energy Storage**

### System B
**Solar PV + Battery Energy Storage + Hydrogen Electrolyzer + Hydrogen Storage + PEM Fuel Cell**

The objective is to determine whether hydrogen can provide a practical form of **long-duration energy storage** while batteries continue to handle shorter-duration energy balancing.

---

# Problem Statement

Rural communities depend on reliable electricity for services that directly affect people's lives.

For a rural healthcare facility, an extended electricity interruption can affect:

- Vaccine refrigeration
- Medical equipment
- Emergency lighting
- Communications
- Water pumping
- Patient services
- Pharmaceutical storage

Solar PV and battery energy storage can provide reliable electricity under normal conditions. However, prolonged periods of low solar generation can exhaust battery reserves.

This research investigates whether hydrogen can provide an additional energy reserve capable of bridging these multi-day renewable-energy deficits.

---

# Research Objectives

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

# Case Study

The research models a representative rural service cluster in **Limpopo, South Africa**, consisting of:

- Rural healthcare clinic
- Vaccine cold-chain refrigeration
- Community water pumping station

The simulated electrical demand includes:

| Load | Power |
|---|---:|
| Vaccine refrigeration | 8 kW |
| Lighting & communications | 4 kW |
| Medical equipment | 4 kW |
| Morning patient surge | +6 kW |
| Evening emergency/water-pumping demand | +15 kW |
| Peak demand | 37 kW |
| Approximate daily energy demand | 468 kWh |

---

# System Configurations

## System A — Battery-Only Baseline

The baseline system consists of:

- 150 kWp solar PV
- 400 kWh lithium-ion battery
- No hydrogen storage
- No electrolyzer
- No fuel cell

The system was intentionally sized with substantial battery capacity to test whether battery storage alone could provide resilience during a prolonged solar deficit.

---

## System B — Hydrogen-Battery Hybrid

The proposed system consists of:

- 150 kWp solar PV
- 120 kWh lithium-ion battery
- 40 kW PEM electrolyzer
- 100 kg hydrogen storage tank
- 40 kW PEM fuel cell
- 65 kg initial hydrogen reserve

The battery provides short-duration energy balancing while hydrogen provides long-duration energy storage.

---

# Core Engineering Concept

The central concept of this research is:

> **Batteries and hydrogen can serve complementary energy-storage roles.**

### Battery

Suitable for:

- Daily energy shifting
- Fast response
- Short-duration storage
- PV smoothing
- Load balancing

### Hydrogen

Suitable for:

- Multi-day energy storage
- Long-duration backup
- Seasonal energy storage
- Extended renewable-energy deficits

The research therefore does not propose replacing batteries with hydrogen.

Instead, it investigates a **hybrid architecture** in which both technologies perform different functions.

---

# Energy Management Strategy

The Energy Management System uses a deterministic priority-dispatch strategy.

When:

```text
P_PV > P_Load
