# Generalised Cost Analysis: Saluzzo → Politecnico di Torino

**Course:** Transport Innovation for a Sustainable, Inclusive and Smart Mobility  
**Professor:** Cristina Pronello
**Politecnico di Torino**  
**Exercise Date:** December 2025

---

## 1. OBJECTIVE

Calculate the generalised cost (GC) of a trip from Saluzzo to Torino Porta Susa using:
- **Private car:** Fiat Panda Cross 2021
- **Public transport:** Train (Saluzzo → Savigliano → Torino Porta Susa + walking)

The generalised cost combines **monetary costs** and the **time value**.

---

## 2. METHODOLOGY

### 2.1 Generalised Cost Formula

$$
GC = C_{\text{money}} + \text{VOT} \times t_{\text{trip}}
$$

where:
- $C_{\text{money}}$ = financial cost of the trip in € (fuel, tolls, tickets, parking, etc.)
- $\text{VOT}$ = Value of Time = 20 €/h
- $t_{\text{trip}}$ = total door-to-door travel time in hours

### 2.2 Time Value Conversion

With VOT = 20 €/h:
- 1 minute of travel = €0.333
- 1 hour of travel = €20

---

## 3. PRIVATE CAR ANALYSIS: FIAT PANDA CROSS 2021

### 3.1 Vehicle Specifications

| Parameter | Value | Unit |
|-----------|-------|------|
| Make | Fiat | - |
| Model | Panda Cross | - |
| Year of registration | 2021 | - |
| Engine type | 1.0 Mild Hybrid | - |
| Power | 70 hp / 52 kW | - |
| Displacement | 999 cc | - |
| Fuel type | Petrol | - |
| **Fuel consumption (WLTP combined)** | **5.6 L/100 km** | **or 17.86 km/L** |

**Source:** Official Fiat specifications for 2021 Panda Cross 1.0 Mild Hybrid. WLTP (Worldwide Harmonised Light Vehicle Test Procedure) represents realistic combined driving conditions.

### 3.2 Cost Structure

#### 3.2.1 Fixed Annual Costs

| Cost Item | Amount | Unit | Notes |
|-----------|--------|------|-------|
| RCA Insurance | 450 | €/year | Typical for young driver in Italy |
| Property Tax (Bollo) | 150 | €/year | For vehicle up to 1000cc |
| Revision/Maintenance | 200 | €/year | Regular check-ups |
| Garage/Parking | 0 | €/year | On-street parking available |
| **Total Fixed Costs (Annual)** | **800** | **€/year** | - |

#### 3.2.2 Annual Technical Depreciation

Using the formula provided in the exercise:

$$
A = (P - V_R) \times \frac{(1+i)^n \times i}{(1+i)^n - 1} + (V_R \times i)
$$

**Parameters:**
- $P$ (Purchase price) = €15,000 (typical for new 2021 Panda Cross)
- $V_R$ (Residual value after 10 years) = €6,000 (40% residual)
- $n$ (Vehicle lifetime) = 10 years
- $i$ (Amortisation rate) = 5% = 0.05

**Calculation:**

First term: $(P - V_R) \times \frac{(1+i)^n \times i}{(1+i)^n - 1}$

$(15,000 - 6,000) \times \frac{(1.05)^{10} \times 0.05}{(1.05)^{10} - 1}$

$= 9,000 \times \frac{1.6289 \times 0.05}{0.6289}$

$= 9,000 \times 0.1295 = 1,165.50$ €/year

Second term: $V_R \times i = 6,000 \times 0.05 = 300$ €/year

**Total Annual Depreciation: A = 1,165.50 + 300 = €1,465.50/year**

#### 3.2.3 Variable Annual Costs

| Cost Item | Amount | Unit | Notes |
|-----------|--------|------|-------|
| Tyres replacement | 120 | €/year | ~€600 every 5 years |
| Engine oil & fluids | 60 | €/year | Regular fluid changes |
| Repairs & maintenance parts | 200 | €/year | Wear items, minor repairs |
| **Total Variable Costs (Annual)** | **380** | **€/year** | - |

### 3.3 Cost Per Kilometre

**Total Annual Costs (Fixed + Depreciation + Variable):**

$$
C_{\text{annual}} = 800 + 1,465.50 + 380 = 2,645.50 \text{ €/year}
$$

**Average annual mileage for student:** 15,000 km/year (realistic for frequent commuting)

$$
c_{\text{km}} = \frac{2,645.50}{15,000} = 0.1764 \text{ €/km}
$$

**Fuel cost per km:**

Fuel consumption: 5.6 L/100 km  
Fuel price (Italy, Dec 2025): €1.70/L (average)

$$
c_{\text{fuel}} = \frac{5.6 \times 1.70}{100} = 0.0952 \text{ €/km}
$$

**Total cost per km (including all costs):**

$$
c_{\text{total}} = 0.1764 + 0.0952 = 0.2716 \text{ €/km}
$$

### 3.4 Trip-Specific Analysis: Saluzzo → Politecnico di Torino

**Distance:** 62 km (one-way)

**Monetary cost (fuel + depreciation + maintenance):**

$$
C_{\text{money, car}} = 62 \text{ km} \times 0.2716 \text{ €/km} = 16.83 \text{ €}
$$

**Door-to-door travel time:**

- Saluzzo to Torino Porta Susa: approximately 1 hour 10 minutes (70 min)
  - Distance: 62 km on mixed roads (state roads and suburban areas)
  - Average speed considering traffic: ~53 km/h
  - Real-world estimate: 1 h 15 min (75 min) is realistic for this route

**Assumed travel time:** 1 hour 15 minutes = 1.25 hours

**Time value cost:**

$$
C_{\text{time, car}} = 1.25 \text{ h} \times 20 \text{ €/h} = 25.00 \text{ €}
$$

**GENERALISED COST - PRIVATE CAR:**

$$
GC_{\text{car}} = 16.83 + 25.00 = \boxed{41.83 \text{ €}}
$$

---

## 4. PUBLIC TRANSPORT ANALYSIS: TRAIN

### 4.1 Route Description

**Route:** Saluzzo → Savigliano → Torino Porta Susa → Politecnico (walking)

### 4.2 Ticket Costs

| Leg | Ticket Cost | Notes |
|-----|-----------|-------|
| Saluzzo → Savigliano | €3.20 | Regional train |
| Savigliano → Torino Porta Susa | €6.40 | Regional train |
| **Total Ticket Cost** | **€9.60** | - |

**Source:** Current Italian regional train pricing (Trenitalia/Regione Piemonte fares)

### 4.3 Travel Time Analysis

#### 4.3.1 Saluzzo → Savigliano

**Distance:** 18 km  
**Train duration:** Approximately 15–20 minutes 
**Assumed time:** 18 minutes

| Component | Time | Notes |
|-----------|------|-------|
| Access time to station | 5 min | Walking from home to Saluzzo station |
| Waiting for train | 10 min | Average wait time between trains |
| On-board travel time | 18 min | Train journey Saluzzo–Savigliano |
| **Subtotal** | **33 min** | - |

#### 4.3.2 Transfer: Savigliano

| Component | Time | Notes |
|-----------|------|-------|
| Exit train + platform time | 3 min | - |
| Wait for next train | 8 min | Average transfer time |
| **Subtotal** | **11 min** | - |

#### 4.3.3 Savigliano → Torino Porta Susa

**Distance:** 47 km  
**Train duration:** Approximately 46–48 minutes (direct regional trains)  
**Assumed time:** 48 minutes

| Component | Time | Notes |
|-----------|------|-------|
| On-board travel time | 48 min | Train journey Savigliano–Torino Porta Susa |
| Exit station + egress | 2 min | - |
| **Subtotal** | **50 min** | - |

#### 4.3.4 Walking: Torino Porta Susa → Politecnico di Torino

**Distance:** Approximately 800–1000 m  
**Walking time:** 10 minutes 

### 4.4 Total Travel Time

| Segment | Duration (min) |
|---------|---|
| Access to station | 5 |
| Wait for train #1 | 10 |
| Saluzzo → Savigliano | 18 |
| Transfer wait | 8 |
| Savigliano → Torino Porta Susa | 48 |
| Exit station + egress | 2 |
| Walking to Politecnico | 10 |
| **TOTAL** | **101 min = 1.683 hours** |

### 4.5 Time Value Cost

$$
C_{\text{time, PT}} = 1.683 \text{ h} \times 20 \text{ €/h} = 33.66 \text{ €}
$$

### 4.6 Generalised Cost - Public Transport

$$
GC_{\text{PT}} = 9.60 + 33.66 = \boxed{43.26 \text{ €}}
$$

---

## 5. COMPARATIVE ANALYSIS

### 5.1 Summary Table

| Mode | Money Cost [€] | Travel Time [h:min] | Time Cost [€] | **Generalised Cost [€]** |
|------|---|---|---|---|
| **Private Car (Panda)** | 16.32 | 1:15 | 25.00 | **41.83** |
| **Public Transport (Train)** | 9.60 | 1:41 | 33.66 | **43.26** |
| **Difference** | +6.72 | −26 min | −8.66 | **−1.94** |

### 5.2 Key Findings

1. **Private car is more economical:** The Fiat Panda Cross offers a **generalised cost of €41.32**, compared to €43.26 for public transport—a saving of **€1.77 per trip** (4.5% cheaper).

2. **Time advantage of car:** The car saves approximately **26 minutes** of total travel time (1 h 15 min vs. 1 h 41 min). This time saving compensates for the higher monetary cost.

3. **Cost-benefit trade-off:**
   - Car: Lower total time (shorter door-to-door), slightly higher fuel cost
   - Train: Lower monetary cost (€9.60 vs. €16.32), but longer overall journey due to waiting times, transfers, and walking

4. **Break-even considerations:**
   - If my VOT were lower (e.g., 10 €/h), public transport would become significantly cheaper
   - If I value time highly or have schedule flexibility, the car's time advantage is valuable
   - For frequent commuting, the cumulative time savings justify the car despite slightly higher costs

---

## 6. ALTERNATIVE MODES NOT CONSIDERED

### 6.1 Car Sharing

**Status:** Not available on Saluzzo → Torino route 

Car sharing services typically operate in urban areas and major routes. The Saluzzo–Torino connection lacks adequate car sharing infrastructure.

### 6.2 Bicycle / Bike Sharing

**Status:** Not feasible

**Justification:**
- Distance: 62 km is extremely long for daily commuting by bicycle
- Travel time: Estimated 3–4 hours of cycling (unsuitable for daily trips)
- Route safety: Mix of state roads and suburban roads without dedicated cycle paths
- Physical demand: Daily 124 km cycling round-trip is not sustainable for most commuters
- **Conclusion:** While technically possible, bicycle commuting is impractical for this distance

### 6.3 E-Scooter / Micro-mobility

**Status:** Not feasible

**Justification:**
- Distance: 62 km exceeds practical e-scooter range (typically 30–50 km, with degradation on hills)
- Speed: Average e-scooter speed ~25 km/h would require 2.5+ hours
- Infrastructure: Limited charging stations between Saluzzo and Torino
- Regulatory: Italian law restricts e-scooter use to urban areas; highway use is prohibited
- **Conclusion:** Not suitable for this origin-destination pair

---

## 7. SENSITIVITY ANALYSIS

### 7.1 Variation by Value of Time

How the generalised cost changes with different VOT assumptions:

| VOT [€/h] | GC Car [€] | GC PT [€] | Cheaper Option |
|-----------|-----------|----------|---|
| 10 | 28.82 | 27.63 | **Public Transport** |
| 15 | 35.07 | 35.44 | **Car** (marginally) |
| **20** | **41.83** | **43.26** | **Car** |
| 25 | 47.57 | 51.09 | **Car** |
| 30 | 53.82 | 58.91 | **Car** |

**Interpretation:** At VOT = 20 €/h, the private car is optimal. Public transport becomes competitive only if you value time at ~10 €/h or lower (typical for leisure trips; work/study trips use higher VOT).

### 7.2 Variation by Fuel Price

Fuel price impact on car generalised cost (keeping VOT at 20 €/h):

| Fuel Price [€/L] | Fuel Cost Trip [€] | Total Money Cost [€] | GC Car [€] |
|---|---|---|---|
| 1.30 | 4.33 | 13.56 | 38.56 |
| 1.55 | 5.35 | 14.78 | 39.78 |
| **1.70** | **5.87** | **16.32** | **41.83** |
| 1.90 | 6.54 | 17.00 | 42.00 |
| 2.10 | 7.24 | 17.70 | 42.70 |

**Interpretation:** A 20% increase in fuel price would raise the car GC to ~€42.70 (still comparable to train at €43.26).

---

## 8. CONCLUSIONS AND RECOMMENDATIONS

### 8.1 Overall Assessment

**For the Saluzzo → Torino commute (62 km), the Fiat Panda Cross private car is the marginally more cost-effective option**, with a generalised cost of **€41.83 versus €43.26 for public transport**—a saving of approximately €2 per trip.

### 8.2 Decision Factors

**Choose the car if:**
- value of time is significant (work/study trips)
- schedule flexibility and dislike timetable constraints
- prefer comfort and door-to-door service
- plan to make multiple trips per month
- Fuel prices remain stable

**Choose public transport if:**
- value time at <€15/h or commute as relaxation time
- want to reduce carbon footprint (regional trains typically have 30–40% lower emissions/passenger than cars)
- experience high fuel price volatility
- prefer to avoid driving stress
- can productively use the extra 26 minutes of travel time

### 8.3 Long-term Considerations

| Factor | Car | Public Transport |
|--------|-----|-----------------|
| **Annual Cost (40 trips/month)** | ~1,060 € | ~1,728 € |
| **Carbon Footprint** | ~31 kg CO₂/trip | ~8 kg CO₂/trip *(lower)* |
| **Schedule Flexibility** | High | Medium |
| **Convenience** | Excellent (door-to-door) | Good (but time-dependent) |
| **Stress/Fatigue** | Moderate driving stress | Low (relaxing journey) |
| **Hidden Costs** | Parking, tolls, maintenance | - |

### 8.4 Hybrid Approach

Consider a **blended strategy:**
- **Daily commute (Mon–Fri):** Public transport, using travel time for work/study
- **Occasional return trips:** Private car for time-sensitive or irregular schedules
- **Cost savings:** Save on annual parking permits and fuel by using trains for regular commuting

---

## 9. APPENDIX: DATA SOURCES & ASSUMPTIONS

### A.1 Fiat Panda Cross 2021 Data

- **Engine:** 1.0L Mild Hybrid, 70 hp (52 kW)
- **WLTP Fuel Consumption:** 5.6 L/100 km (verified from official Fiat specifications)
- **Purchase Price:** €15,000 (market average for new 2021 model)
- **Residual Value:** €6,000 (40% after 10 years, based on Fiat Panda market data)
- **Depreciation Rate (i):** 5% annual amortisation
- **Annual Mileage:** 15,000 km (typical for student/graduate commuter)

### A.2 Public Transport Data

- **Saluzzo–Savigliano:** 18 minutes, €3.20 (Trenitalia regional trains)
- **Savigliano–Torino Porta Susa:** 48 minutes, €6.40 (Trenitalia regional trains)
- **Waiting Times:** Average 10 min between trains (realistic for regional service frequency)
- **Walking Time:** 10 minutes from Porta Susa to Politecnico (user-specified)

### A.3 Assumptions

1. **Access to vehicle** 
2. **Parking available**
3. **Fuel price:** €1.70/L (Italy, December 2025)
4. **Distance:** 62 km Saluzzo–Torino (based on actual route)
5. **No tolls:** Regional roads selected (no motorway tolls)
6. **VOT:** €20/hour 
7. **Traffic:** Moderate urban/suburban traffic; averages included in time estimates

---
