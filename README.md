# PULESS
### Passive Ultra-Lightweight Electrostatic Stabilization System

**A Zero-Power Electrostatic Discharge (ESD) Mitigation Architecture for Lunar Surface Operations**


## 🌕 Overview

**PULESS (Passive Ultra-Lightweight Electrostatic Stabilization System)** is a proposed passive electrostatic discharge mitigation architecture designed for NASA Artemis lunar surface operations.

The system aims to reduce electrostatic charging hazards affecting:

- Lunar Extravehicular Activity (EVA) suits.
- Lunar Terrain Vehicles (LTVs).
- Pressurized lunar airlocks.
- Astronaut equipment and external suit interfaces.

Lunar regolith is highly insulating and can accumulate electrostatic charge through surface interactions. During lunar traverses, this can create significant potential differences between spacesuits and grounded infrastructure.

PULESS introduces a lightweight, zero-power, multi-layer charge-management architecture that combines equipotential conductive materials, passive resistive discharge, dust-tolerant electrical contacts, and an optional field-emission mechanism.

**Core Concept:** Reduce electrostatic discharge hazards without relying on batteries, active plasma systems, or propellant.

> **Development status:** Analytical concept (TRL 2–3). All performance values are preliminary design targets or analytical estimates pending experimental validation.

---

## 🚀 The Problem

The lunar environment presents unique electrostatic challenges.

Unlike Earth, the Moon lacks a dense atmosphere and has extremely dry, electrically insulating surface materials. Interactions between spacesuits and lunar regolith can contribute to charge accumulation.

Two distinct hazards must be considered.

### 1. External Electrostatic Discharge

During lunar surface operations, a charged spacesuit approaching a grounded metallic structure may experience a sudden potential equalization.

Potential consequences include:

- Electrical arcing at conductive interfaces.
- Electromagnetic interference with suit avionics.
- Damage to sensitive electronic components.
- Surface degradation at electrical contact points.
- Risks to airlock interface components.

### 2. Internal Electrostatic Discharge

Electrostatic charge may remain localized on insulating suit materials even after an astronaut enters a pressurized environment.

During airlock repressurization, discharge between isolated conductive or charged regions could present an ignition concern in oxygen-enriched environments.

This hazard requires separate investigation and validation.

### Why Existing Solutions Are Challenging

Active electrostatic mitigation systems can require:

- Electrical power.
- Additional hardware and volume.
- Propellant or consumables.
- Integration with spacecraft electrical systems.
- Additional maintenance and operational complexity.

PULESS explores a passive alternative designed to minimize these requirements.

---

## ⚙️ System Architecture

PULESS uses a four-layer defense-in-depth architecture.

### Layer 1 — Equipotential Suit Shell

**Proposed materials:** 316L stainless-steel conductive elements and carbon nanotube (CNT) yarn.

Integrated into the suit's Beta-cloth outer layer, this conductive network is intended to distribute electrostatic charge and reduce localized charge accumulation.

**Primary function:**
- Improve surface charge distribution.
- Reduce localized potential differences.
- Provide a conductive path toward the discharge interface.

### Layer 2 — Dual-Redundant Ceramic Bleed Resistor

**Proposed resistance:** 10 MΩ.

A passive resistive discharge mechanism is integrated into the safety tether cuff.

When connected to a suitable grounded handrail, the resistor provides a controlled discharge path.

**Primary function:**
- Limit discharge current.
- Reduce sudden charge transfer.
- Provide passive charge equalization.
- Maintain a redundant discharge architecture.

### Layer 3 — Anti-Cold-Weld TiN Contact Tip

**Proposed material:** Titanium Nitride (TiN).

A TiN-coated contact tip is incorporated into the tether carabiner to investigate improved contact durability and reduced cold-welding susceptibility.

The contact interface is intended to maintain electrical continuity while interacting with dust-contaminated surfaces.

### Layer 4 — Optional Tungsten Field Emitter

A passive tungsten field-emission component is proposed as an additional charge-management mechanism during extended traverses away from grounded infrastructure.

**Intended function:**
- Investigate passive charge dissipation into the surrounding vacuum.
- Provide a supplementary mechanism during untethered surface operations.

Its effectiveness under realistic lunar environmental conditions requires experimental verification.

---

## 🔌 Electrical Discharge Model

PULESS uses a simplified RC discharge model to estimate the time required to reduce the electrostatic potential of a charged suit.

### Design Parameters

| Parameter | Symbol | Proposed Value |
|---|---|---:|
| Suit capacitance | C | 200 pF |
| Initial potential | V₀ | 5,000 V |
| Bleed resistance | R | 10 MΩ |
| RC time constant | τ | 2.0 ms |
| Time to 99% discharge | t₉₉ | 9.21 ms |
| Initial discharge current | I₀ | 0.50 mA |
| Initial stored energy | E | 2.50 mJ |

### Governing Equations

**RC Time Constant**

τ = RC

τ = (10 × 10⁶) × (200 × 10⁻¹²)

τ = 2.0 ms

**Voltage Decay**

V(t) = V₀e⁻ᵗ/ᴿᶜ

**Discharge Current**

I(t) = (V₀/R)e⁻ᵗ/ᴿᶜ

**Stored Electrostatic Energy**

E = ½CV₀²

E = ½ × 200 × 10⁻¹² × 5000²

E = 2.50 mJ

**Time to 99% Discharge**

t₉₉ = RC ln(100)

t₉₉ ≈ 9.21 ms

These calculations represent an idealized single-capacitance, single-resistance model. Actual suit charging, distributed capacitance, contact impedance, and discharge behavior may differ.

---

## 📊 Key Specifications

| Specification | Value |
|---|---|
| Project Name | PULESS |
| Full Form | Passive Ultra-Lightweight Electrostatic Stabilization System |
| Technology Readiness | TRL 2–3 (conceptual) |
| Proposed Mass | 47 g |
| Electrical Power | 0 W |
| Proposed Thermal Design Range | −240°C to +200°C |
| Primary Application | Lunar EVA Systems |
| Secondary Applications | LTVs and Pressurized Airlocks |
| Architecture | Four-layer passive mitigation |
| Primary Discharge Mechanism | Resistive charge equalization |

*Mass and thermal range are preliminary design targets, not verified component-level or system-level qualifications.*

---

## 🛰️ Potential Applications

### Artemis Lunar EVA Suits
Passive charge-management integration for astronaut spacesuits operating on the lunar surface.

### Lunar Terrain Vehicles
Investigation of electrostatic mitigation for vehicle surfaces, interfaces, and astronaut contact points.

### Pressurized Airlocks
Controlled charge equalization during suit-to-airlock electrical connection and ingress operations.

### Lunar Infrastructure
Potential integration into conductive handrails, docking interfaces, equipment enclosures, and other grounded infrastructure.

---

## 🧪 Development & Validation Roadmap

PULESS is currently at the analytical concept stage. The following roadmap outlines the proposed development and validation process.

### Phase 1 — Initial Bench Testing
- [ ] Construct a 10 MΩ resistive discharge prototype.
- [ ] Validate RC discharge behavior using an ESD simulator.
- [ ] Capture voltage and current waveforms using an oscilloscope.
- [ ] Compare measured discharge times against analytical predictions.

### Phase 2 — Material Screening
- [ ] ASTM E595 outgassing screening.
- [ ] NASA-STD-6001B material flammability and compatibility assessment.
- [ ] Evaluate conductive CNT-based textile integration.
- [ ] Evaluate TiN-coated electrical contact performance.

### Phase 3 — Cryogenic and Thermal Vacuum Testing
- [ ] Thermal-vacuum cycling.
- [ ] Low-temperature material characterization.
- [ ] Contact resistance measurements.
- [ ] Thermal cycling durability assessment.
- [ ] Preliminary target: 100+ cycles.

### Phase 4 — Lunar Dust and ESD Validation
- [ ] Dust-contaminated electrical contact testing.
- [ ] LHS-1 lunar regolith simulant testing.
- [ ] Vacuum discharge characterization.
- [ ] Suit-equivalent electrostatic charging experiments.
- [ ] Evaluate performance under single-component failure conditions.

### Phase 5 — Research Dissemination
- [ ] Prepare technical research documentation.
- [ ] Submit a proposed white paper to relevant lunar surface innovation programs.
- [ ] Investigate potential collaboration with aerospace research institutions.

---

## ⚠️ Engineering Risks & Open Questions

The following issues must be addressed before PULESS can be considered suitable for human-rated lunar operations.

| Risk | Required Investigation |
|---|---|
| Conductive textile integration | Flexibility, abrasion, electrical continuity |
| Resistor reliability | Redundancy and open/short-circuit failure analysis |
| Dust contamination | Contact resistance and discharge reliability |
| TiN interface | Contact stability and cold-welding resistance |
| Tungsten emitter | Field-emission feasibility in lunar vacuum |
| Oxygen compatibility | Ignition and material compatibility testing |
| Thermal extremes | Component performance and material degradation |
| Human safety | Shock, current-path, and fault-condition analysis |

**Important:** A low calculated RC discharge current does not establish human electrical safety or eliminate ignition risk. The actual current path, localized discharge energy, material flammability, and oxygen compatibility must be independently assessed.

---

## 📚 Standards & Technical References

The following documents provide relevant engineering guidance for further development:

1. **NASA-HDBK-4002B** — Mitigating In-Space Charging Effects.
2. **NASA-STD-6001B** — Flammability, Offgassing, and Compatibility in Oxygen-Enriched Environments.
3. **ASTM E595** — Standard Test Method for Total Mass Loss and Collected Volatile Condensable Materials from Outgassing in a Vacuum Environment.

These references are starting points for engineering assessment. Their applicability and current revisions should be confirmed before establishing a formal qualification or verification plan.

---

## 📁 Repository Structure

```text
PULESS/
│
├── README.md
│
├── docs/
│   └── PULESS_Technical_Memorandum.docx
│
├── diagrams/
│   ├── system_architecture.png
│   └── discharge_path.png
│
├── simulations/
│   └── README.md
│
├── cad/
│   └── README.md
│
├── testing/
│   └── README.md
│
└── research/
    └── references.md
```

---

## 🎯 Project Objective

The objective of PULESS is to investigate whether a lightweight, passive, zero-power electrostatic mitigation architecture can improve the safety and reliability of lunar surface operations.

By combining conductive materials, controlled resistive discharge, dust-tolerant contacts, and an optional field-emission mechanism, the concept aims to address electrostatic hazards across multiple lunar operational environments.

**PULESS — Passive Protection for the Next Generation of Lunar Exploration.**

---

## 📌 Project Status

**Current Stage:** Analytical Concept Development

**Technology Readiness Level:** TRL 2–3 (proposed)

**Experimental Validation:** Pending

**NASA Affiliation or Endorsement:** Not claimed. This is an independent engineering concept and is not an officially approved NASA system.

**Contributions:** Research, simulation, material evaluation, electrical modeling, and experimental validation contributions are welcome.
