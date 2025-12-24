# Urban Building Energy Modelling: Energy Consumption for Space Heating

**Authors:** Alesso Tommaso Maria (s337250), Difino Chiara (s343806), Mojica Ardila Natalia (s334735)

---

## Abstract

In response to the urgent need for energy transition and climate change mitigation, this study applies Urban Building Energy Modelling (UBEM) to assess building energy performance at the district scale. A GIS-based framework is used to estimate the energy consumption of the residential building stock in the Crocetta district of Turin using key geometric and statistical variables. Retrofit scenarios are evaluated through energy and economic indicators, including annual savings and simple payback time, to support informed decision making and climate-responsive urban planning.

---

## 1. Introduction

Urban Building Energy Modelling (UBEM) is an emerging approach that enables the simulation and analysis of the energy performance of buildings within an urban context. Its importance lies in providing quantitative information to support urban planning, strategic decision making and energy policy formulation. Among the main benefits of UBEM is the identification of energy savings and emissions reduction opportunities[1].

This relevance becomes evident when considering that, in 2015, cities were estimated to be responsible for approximately two thirds of global energy consumption and more than 70% of global CO₂ emissions[2], with urban buildings responsible for nearly 60% of total building final energy use[3]. In Italy, the civil sector represented approximately 26% of total final energy consumption in 2023, highlighting the critical role of buildings in national energy demand and the need for effective strategies to reduce energy use in the built environment.

Beyond technical improvements, the economic feasibility of retrofit interventions is a key factor in their large-scale adoption. Evaluating retrofit measures therefore requires integrating energy performance assessments with economic indicators such as investment costs, annual energy savings and simple payback time, to support effective and equitable energy efficiency policies.

The aim of this report is to estimate the energy consumption of the existing residential building stock in the Crocetta district of Turin, Italy, and to analyse and improve its energy efficiency through retrofit measures using the UBEM methodology. The approach is based on a GIS model to calculate the Energy Performance Index (EP) of each building, predicted from key geometric and statistical variables, including building dimensions, construction period and the surface-to-volume ratio (S/V)[4].

GIS-based UBEM is a critical tool for enhancing energy efficiency and promoting sustainable urban development. It provides a framework for collecting, managing, analysing and visualising large-scale spatial and building data[5]. Since modelling and geometric data are a fundamental part of the methodology, GIS plays a central role in identifying and visualising buildings data and their distribution, supporting decision-making, at urban and regional scale[3].

On this basis, the following sections present the application of the GIS based UBEM framework to a real urban context, illustrating how building scale data can be integrated at the district level to support energy performance assessment and retrofit analysis.

---

## 2. Case Study Description

The case study focuses on the Crocetta district, located south of the historic city centre of Turin, Italy. The district covers an area of approximately 2.51 km² and comprises a total of 628 buildings, of which 559 are residential, accounting for 89.01% of the building stock.

Most residential buildings (88.91%) were constructed during the modern era, with a particularly high concentration in the 1919–1945 construction period, representing 39.89% of the residential stock.

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_1_Construction_Period.png}
\caption{Map of the construction periods of the residential buildings in the Crocetta neighbourhood, Turin}
\label{fig:Construction}
\end{figure}

Crocetta experiences climatic conditions that generate a substantial space heating demand, as indicated by an average annual temperature of 11.22 °C and an absolute minimum temperature of −5.63 °C in the province of Torino in 2024, which contribute to increased heating energy requirements[6].

Building footprint, construction period, and geometric attributes were obtained from municipal GIS datasets and used as input for the UBEM analysis, as summarized in Table 1.

\begin{table}
\centering
\caption{Necessary Dataset for the Urban Building Energy Modelling Exercise}
\label{tab:data_summary}
\begin{tabular}{|l|l|l|l|l|l|}
\hline
\textbf{Typology} & \textbf{Input Data} & \textbf{Typology (Data/Field)} & \textbf{Description} & \textbf{Source} & \textbf{License} \\
\hline
\multirow{5}{*}{Built-Up Environment} & Building Shapes & Torino -- BDTRE & Building outlines (filtered for height > 3m, area 50--3000 m²) & Geoportale & CC BY 4.0 \\
\cline{2-6}
& Building Uses & Torino -- BDTRE (edifuso) & Building function data & Geoportale & CC BY 4.0 \\
\cline{2-6}
& Construction Period & Torino -- R01-indicatori & Year of construction by block & ISTAT & CC BY 3.0 \\
\cline{2-6}
& Building Heights & Torino -- BDTRE (unvolav) & Number of floors & Geoportale & CC BY 4.0 \\
\cline{2-6}
& Admin. Information & Torino -- Circoscrizioni & Administrative boundaries & Geoportale & CC BY 4.0 \\
\hline
Socio-Economic & Population, Housing, Income & ISTAT & Census and territory data & ISTAT & CC BY 3.0 \\
\hline
Climate Data & Solar Irradiation & EX2 & Solar radiation potential & Exercise 2 & -- \\
\hline
Energy Consumption & Natural Gas, Space Heating & Numerical Data & Annual heating energy calculation & EIA Surveys & Open Data \\
\hline
\end{tabular}
\end{table}

---

## 3. Literature Review and Theoretical Background

### 3.1 Urban Building Energy Modelling (UBEM)

Urban Building Energy Modelling (UBEM) is a computational methodology for modelling energy use in the urban context, enabling the analysis of the energy performance of a stock of buildings, from a block to a national scale. It uses factors such as geometry, building materials, occupancy patterns and energy systems to simulate buildings energy consumption and create energy models for individual buildings or groups of buildings. In recent years, this technology has gained popularity in the urban, energy and political sector, as it supports decisions on design, rehabilitation and urban development[1].

In the context of the energy transition, its use becomes imperative, since among its applications are:
- Efficient design and optimization of urban buildings
- Evaluation of energy saving and carbon reduction strategies[7]
- Analysis of building-to-building interaction and District-level network technologies
- Support for urban resilience policies and renovation planning[8]
- Evaluating building retrofit options
- Assessment of rehabilitation and functional conversion scenarios[9]

However, challenges such as the availability and quality of data, computational requirements, calibration and validation of the model, and the impact of local factors (urban micro-climate and interaction between buildings), could affect results and significantly increase uncertainty[7][3].

Three steps are required to complete the process: data entry, thermal model creation and execution, and validation/calibration of results. The literature indicates that the following types of data are typically required:

\begin{itemize}
\item \textbf{Geometrical data:} shape, location, number of floors of buildings, footprint area, total area, gross heated surface, window--wall ratio, usage, period of construction and renovation[10].

\item \textbf{Weather data:} accurate meteorological files reflecting urban micro-climatic conditions, including external temperature, humidity, wind direction and velocity, solar radiation, Urban Heat Islands (UHI) effects and extreme climate effects[11].

\item \textbf{Additional data (non-geometric data):} thermal parameters of building elements, occupation profiles and number of occupants, patterns of equipment use and operating hours, HVAC system efficiency and composition, type of heating system, annual consumption of electricity and natural gas, lighting profiles and appliances[11].

\item \textbf{Validation and calibration data:} such as measured energy consumption, national or local survey data, energy reports, open data sources, energy performance certificates (EPC)[12], and performance metrics[13].
\end{itemize}

#### 3.1.1 Top-Down Approach

This approach starts the analysis from a macro-level perspective and progressively moves towards a more disaggregated scale. It relies on aggregated input data, such as total energy consumption at the sectoral or city level and examines its variation as a function of external factors including economic activity, demography, and climatic conditions. The consumption is then distributed across different sectors or building categories. However, this approach does not delve into the details of technologies and consumption profiles at the level of individual buildings or specific areas, since it is focused on the link between macroeconomic variables and energy consumption[14].

#### 3.1.2 Bottom-Up Approach

This approach begins the analysis from the characteristics of single buildings, modelling their physical properties (windows, walls) and then aggregates these elements to the urban level. It is limited by the need for large quantities of technical data; nevertheless, it has a high level of detail, useful to generate a quantitative perspective that guides urban building design and energy policy formulation[14].

### 3.2 Key Variables in Heating Consumption

Energy consumption for space heating depends on three key variables: building dimensions (mainly the volume and useful surface heated), construction period, and S/V ratio[4].

**Construction Period:** One of the most influential variables. The age of construction of the buildings determines the materials, type of envelope and levels of thermal insulation used. Because of this, buildings constructed in different eras exhibit varying levels of thermal insulation and system efficiency. Key dates in Italy, such as Law 373/1976 and Law 10/91, mark significant shifts in energy efficiency standards.

**Surface-to-Volume Ratio (S/V):** Known as the "non-compactness" factor. This ratio measures the heat loss area in proportion to the heated gross volume. A high S/V value indicates a larger heat loss area relative to the volume, resulting in higher space heating energy demand.

**Heat Loss Surface (S):** The total building envelope area through which heat is lost.

**Gross Heated Volume (V):** Represents the total space contained within a building envelope that requires heating.

The formulas for these key concepts are:

$$S = (A_{fp} \times 2) + (P \times H) \quad [m^2]$$

$$V = A_{fp} \times H \quad [m^3]$$

$$\frac{S}{V} = \frac{\text{Heat Loss Surface}}{\text{Heated Gross Volume}}$$

Where:
- $S$ = Heat Loss Surface (m²)
- $V$ = Gross Heated Volume (m³)
- $A_{fp}$ = Footprint Area (m²)
- $P$ = Building Perimeter (m)
- $H$ = Building Height (m)

#### 3.2.1 Adjustments for Adjoining Buildings

When buildings are adjoining, a portion of their external envelope is not exposed to the outdoor environment and therefore does not contribute to heat losses.

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_2_CommonWalls.png}
\caption{Common walls between two adjacent buildings}
\label{fig:CWalls}
\end{figure}

For adjoining buildings, the S/V ratio is adjusted by subtracting the walls in common. A building with many common walls will have a much lower S/V ratio—and thus better thermal efficiency—than an isolated building of the same size[4].

$$S_{\text{common}} = L_{\text{common}} \times H_{\text{min}} \quad [m^2]$$

Where:
- $S_{\text{common}}$ = Surface area of the common wall (m²)
- $L_{\text{common}}$ = Length of the shared boundary between buildings (m)
- $H_{\text{min}}$ = Height of the shorter building (m)

The Real Heat Loss Surface and Real Heated Volume are calculated as:

$$S_{\text{real}} = S - S_{\text{common}} \quad [m^2]$$

$$V_{\text{real}} = V - (S_{\text{common}} \times 0.4) \quad [m^3]$$

The initial S/V ratio is then adjusted using a multiplicative factor based on building typology:

\begin{table}
\centering
\caption{Building typology and corresponding S/V ratio conversion factors}
\label{tab:sv_factors}
\begin{tabular}{|l|c|c|}
\hline
\textbf{Building Typology} & \textbf{S/V Ratio range [m²/m³]} & \textbf{Mult. Factor} \\
\hline
Detached house & $\frac{S}{V} > 0.71$ & 1.31 \\
\hline
Terrace house / Little row house (max 3 floors) & $0.56 < \frac{S}{V} \leq 0.71$ & 1.25 \\
\hline
Big row house / Large apartment block (> 3 floors) & $0.45 < \frac{S}{V} \leq 0.56$ & 1.21 \\
\hline
Tower / Large compact multi-family building & $\frac{S}{V} \leq 0.45$ & 1.08 \\
\hline
\end{tabular}
\end{table}

$$(S/V)_{\text{real}} = (S/V)_{\text{init}} \times F_{\text{building}}$$

### 3.3 Energy Performance Metrics

Energy performance is the key metric to Urban Building Energy Modelling (UBEM), since its analysis and optimization enables maximizing energy efficiency and is the basis for urban design, planning, retrofitting and energy policy decisions[15].

The European Directive on the Energy Performance of Buildings (EPBD) defines energy performance as the annual amount of energy consumed or expected to be consumed, to meet the requirements associated with the standardized use of the building, which include winter and summer air conditioning, domestic hot water production, ventilation, and lighting[16].

Within this regulatory framework, Energy Performance Certificates (EPC) represent an operational instrument for assessing and communicating building energy performance.

#### 3.3.1 Energy Performance Index (EPI)

The Energy Performance Index (EPI) is a widely used metric for assessing buildings energy performance. It is also commonly referred to as Energy Use Intensity (EUI) or Building Energy Index (BEI). It is typically expressed in kWh/m²/year, as it represents the annual primary energy consumption of a building divided by the heated gross floor area of the building per year[17]:

$$\text{EPI} = \frac{E_{\text{annual}}}{\text{Gross Floor Area}} \quad [kWh/(m^2 \cdot year)]$$

#### 3.3.2 Energy Class

Energy Class System in Italy is a method for labelling the energy performance of buildings, designed to promote energy efficiency and support national and European decarbonization targets. The energy class can be evaluated by the average energy performance index reported by ENEA.

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_3_EnergyClass.png}
\caption{Classification of the building stock by EP classes}
\label{fig:EClass}
\end{figure}

#### 3.3.3 Gross Heated Surface and Useful Heated Surface

The gross heated surface (GHS) refers to the total heated floor area of a building, calculated as the product of each floor area by the number of floors in the building:

$$\text{GHS} = A_{\text{floor}} \times N_{\text{floors}} \quad [m^2]$$

The number of floors is calculated by dividing the height of the building by the average gross height. For Turin, the Average Gross Height for buildings constructed before 1970 can be considered as 3.3 meters and 3 meters for buildings constructed after 1970[4].

The Useful Heated Surface refers to the net area taken into account for heating energy consumption. It is computed from the Gross Heated Surface by applying a correction factor ($f_n$) which depends on the average wall thickness ($d_m$)[4]:

$$\text{UHS} = \text{GHS} \times f_n \quad [m^2]$$

$$f_n = 0.9761 - (0.3055 \times d_m)$$

The wall thickness depends on the construction period:

\begin{table}
\centering
\caption{Assumed wall thickness based on construction period}
\label{tab:dm}
\begin{tabular}{|l|c|}
\hline
\textbf{Construction Period} & \textbf{Wall Thickness (m)} \\
\hline
Before 1950 & 0.50 \\
\hline
1950--1976 & 0.30 \\
\hline
1976--1991 & 0.35 \\
\hline
After 1991 & 0.40 \\
\hline
\end{tabular}
\end{table}

#### 3.3.4 Space Heating Consumption and Energy Cost

The energy consumption for space heating ($EC_H$) is the annual energy consumption a building requires to maintain temperature in its indoor spaces[4]. It is expressed in kilowatt-hours per year (kWh/year).

The annual energy consumption is calculated by multiplying the EP by the net heated area and dividing by the conversion factor $f_p$:

$$\text{EC}_H = \frac{\text{EP} \times m^2}{f_p} \quad [kWh/year]$$

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_4_FP.png}
\caption{Conversion factor ($f_p$) for calculating annual consumption for space heating (kWh/year)}
\label{fig:FP}
\end{figure}

The cost of consumption for space heating depends on the fuel used. In Italy, the cost of natural gas is approximately 0.11 €/kWh (October 2025)[4]:

$$EC_{\text{cost}} = P_{\text{ng}} \times EC_{\text{annual}} \quad [€/year]$$

Where:
- $EC_{\text{cost}}$ = Annual energy cost for space heating (€/year)
- $P_{\text{ng}}$ = Up-to-date price of natural gas per energy unit (€/kWh)
- $EC_{\text{annual}}$ = Annual energy consumption (kWh/year)

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_5_CostFuels.png}
\caption{Average costs for fuel type}
\label{fig:CostFuel}
\end{figure}

Certain areas of Turin are served by a district heating (DH) network, for which energy costs differ from those of individual gas systems:

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_6_DH.png}
\caption{DH network distribution}
\label{fig:DH}
\end{figure}

### 3.4 Interventions and Economic Evaluation in UBEM

UBEM is key to assessing the impact of retrofit programs and energy transition policies, allowing for continuous monitoring and optimization of energy performance after implementation of measures.

Retrofit measures (or improvement interventions) are actions implemented with the objective of improving the energy efficiency of the existing building stock. The types of intervention may include:

\begin{itemize}
\item Replacement of windows
\item Insulation of roofs
\item Insulation of the lower slab
\item Insulation of vertical walls (only for buildings built after 1960)
\item Overall retrofit (greater impact but high cost per square meter)
\item Replacement of the condensing boiler
\end{itemize}

#### 3.4.1 Economic Viability

Economic viability is measured through the Simple Payback Time (SPT), which is calculated by dividing the cost of the intervention by the annual economic savings[4]:

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_7_SimplePBT.png}
\caption{Simple Payback Time (SPT) calculation}
\label{fig:SPBT}
\end{figure}

In Italy, tax deductions represent a key policy instrument to economically support building owners in improving energy performance through retrofit interventions:

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_8_IncentivesItaly.png}
\caption{Incentives in Italy with tax deduction in 2024-25}
\label{fig:IncTax}
\end{figure}

The maximum allowable expenditure thresholds for energy efficiency retrofit interventions are established by Italian Decree of 14 February 2022:

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_9_AllegatoA.png}
\caption{Specific maximum costs defined for the appropriateness of retrofit expenses}
\label{fig:AllegatoA}
\end{figure}

The investment cost for each intervention is calculated as:

$$C_{\text{inv}} = A_{\text{comp}} \times C_{\text{int}} \quad [€]$$

Where:
- $C_{\text{inv}}$ = Total investment cost (€)
- $A_{\text{comp}}$ = Component surface area (m²)
- $C_{\text{int}}$ = Specific intervention cost (€/m²)

For comprehensive retrofit interventions, a maximum cost of approximately 1200 €/m² is defined, applied to the conditioned usable floor area of the building[4].

The effectiveness of energy efficiency interventions is evaluated through the assessment of annual energy and economic savings:

$$S_{\text{annual}} = C_{\text{annual,init}} - C_{\text{annual,after}} \quad [€/year]$$

Where:
- $S_{\text{annual}}$ = Annual energy savings (€/year)
- $C_{\text{annual,init}}$ = Initial annual energy cost
- $C_{\text{annual,after}}$ = Annual energy cost after the intervention

---

## 4. Retrofit Scenarios and Economic Assessment

The study examined multiple retrofit scenarios for the Crocetta district. Key findings include:

\begin{table}
\centering
\caption{Economic Impact and Cost-Effectiveness of Retrofit Interventions}
\label{tab:financial}
\small
\begin{tabular}{|l|c|c|c|c|c|c|c|}
\hline
\textbf{Retrofit Measure} & \textbf{Eligible} & \textbf{Total Savings} & \textbf{Cost of} & \textbf{SPT} & \textbf{SPT After} & \textbf{Cost-} \\
& \textbf{Buildings} & \textbf{(€/Year)} & \textbf{Intervention} & \textbf{Before} & \textbf{(36\% tax)} & \textbf{Effectiveness} \\
\hline
Roof Insulation & 558 & €2,285,294.84 & €48,985,307.19 & 16.49 y & 10.55 y & 4.67\% \\
\hline
Window Replacement & 558 & €2,012,770.86 & €63,521,154.42 & 22.06 y & 14.12 y & 3.17\% \\
\hline
Slab Insulation & 558 & €723,457.55 & €31,946,939.47 & 37.07 y & 23.73 y & 2.26\% \\
\hline
Wall Insulation & 137 & €1,022,008.67 & €24,127,975.15 & 17.90 y & 11.46 y & 4.24\% \\
\hline
Overall Retrofit & 558 & €6,615,303.53 & €781,798,823.69 & 82.37 y & 52.72 y & 0.85\% \\
\hline
\end{tabular}
\end{table}

Beyond the 36% tax deduction scenario, a higher incentive level (70%) was tested to explore the maximum reduction of investment risk:

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_10_SPT70_Windows.png}
\caption{SPT: Windows Substitution with 70\% incentive}
\label{fig:SPT_WS_70}
\end{figure}

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_11_SPT70_Roof.png}
\caption{SPT: Roof Insulation with 70\% incentive}
\label{fig:SPT_RI_70}
\end{figure}

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_12_SPT70_Slab.png}
\caption{SPT: Lower Slab Insulation with 70\% incentive}
\label{fig:SPT_LSI_70}
\end{figure}

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_13_SPT70_Walls.png}
\caption{SPT: Vertical Walls Insulation with 70\% incentive}
\label{fig:SPT_VWI_70}
\end{figure}

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_14_SPT70_Overall.png}
\caption{SPT: Overall retrofit with 70\% incentive}
\label{fig:SPT_Overall_70}
\end{figure}

At district level, the average EP falls from approximately 182 kWh/m²/year in the baseline to about 151 kWh/m²/year after window replacement, 143 kWh/m²/year after roof insulation, 171–172 kWh/m²/year after lower slab insulation and around 171 kWh/m²/year after vertical wall insulation, while the combined scenario reduces EP to roughly 103 kWh/m²/year.

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_15_DensityEP.png}
\caption{Density plot of EP before and after overall retrofit}
\label{fig:DensityEP}
\end{figure}

---

## 5. Socio-Economic and Distributional Analysis

To integrate distributional aspects into the assessment, a household energy burden indicator was computed as the ratio between annual heating expenditure and disposable income at census-block level:

\begin{figure}
\centering
\includegraphics[width=\textwidth]{IMAGE_PLACEHOLDER_16_EnergyBurden.png}
\caption{Classification of the residential building stock in Crocetta by the Household Energy Burden Indicator}
\label{fig:EnergyBurden}
\end{figure}

This indicator highlights the blocks where households are more vulnerable to energy price increases and where retrofit support should be prioritised.

---

## 6. Conclusions

This study demonstrates that a GIS-based UBEM framework can effectively quantify space-heating demand, economic costs and retrofit potential at the district scale, using Crocetta as a representative high-density residential neighbourhood in Turin. The analysis shows that building geometry (real S/V ratio), construction period and useful heated surface are the key drivers of energy performance, with EP increasing with non-compactness and older construction periods, while annual consumption scales almost linearly with UHS.

The baseline stock is characterised by a predominance of tower-type multi-family buildings from the 1919–1970 periods, with average EP around 170–190 kWh/m²/year and energy classes concentrated in D–F, resulting in district-wide annual consumptions exceeding 10⁸ kWh/year and average building-level costs of about 20,000 €/year. Mid-century buildings account for the majority of total heating demand and GHG emissions, despite the presence of more efficient recent constructions.

Retrofit simulations indicate that individual measures such as window substitution and roof insulation can reduce average EP by 15–20% and annual consumption by up to 20%, whereas the combined overall scenario achieves a reduction of approximately 40–45% in both EP and energy use, shifting the EP distribution peak from around 180 to about 100 kWh/(m²·year). These improvements correspond to substantial cost savings (about 9,300 €/year per building on average for overall retrofit) and significant GHG reductions, particularly in large multi-family blocks.

However, economic viability remains a major constraint: without incentives, most envelope interventions exhibit simple payback times exceeding 30 years, and even under 50–80% tax deductions only a subset of high-consumption towers achieve SPT values below 15–20 years. Combined with the household energy-burden indicator, this suggests that retrofit programmes should be targeted rather than uniform, prioritising buildings where energy savings, payback time and social vulnerability align.

### Policy Recommendations

From a policy and planning perspective, three main recommendations emerge:

1. **Focus on Mid-Century Residential Blocks:** Municipal and regional strategies should focus on the mid-century residential blocks that dominate Crocetta's heating demand, using UBEM outputs to identify the most impactful interventions at building and block scale.

2. **Promote Integrated Retrofit Packages:** Integrated retrofit packages—combining windows, roof, wall and slab insulation—should be promoted for selected high-consumption buildings, rather than dispersing resources across isolated measures with limited effect.

3. **Integrate Socio-Economic Metrics:** Socio-economic metrics such as energy burden should be explicitly integrated into district-scale prioritisation frameworks, ensuring that financial incentives support both emissions reduction and energy-poverty mitigation in vulnerable areas.

Overall, the Crocetta case study confirms that GIS-based UBEM can serve as a powerful decision-support tool for climate-responsive urban planning, enabling the coupling of technical, economic and social criteria to design effective and equitable renovation strategies for existing urban building stocks.

---

## References

[1] Zhang, X., et al. (2025). Urban building energy modelling: A comprehensive review. *Journal of Building Engineering*, 112428.

[2] Shen, L., et al. (2023). Global energy consumption and emissions in cities. *Sustainable Cities and Society*, 105803.

[3] Torabimoghadam, P., et al. (2018). Energy modelling of urban building stocks. *Building and Environment*, 147, 70–85.

[4] exClass (2024). Energy Performance Index calculations and building efficiency standards. Course material.

[5] Ali, U., et al. (2020). GIS-based building energy assessment. *GIS-based Solutions*, 115834.

[6] OpenLayers Map (2024). Climate data for Turin Province. Retrieved from temperature records.

[7] Alchapar, N., et al. (2024). Retrofit scenarios and energy transition policies. *Energy Policy*, 114468.

[8] Yang, Y., et al. (2025). Building rehabilitation and functional conversion. *Sustainable Development Review*, 113030.

[9] Song, X., et al. (2025). Top-down and bottom-up UBEM approaches. *Urban Planning Review*, 106147.

[10] Fernández, J., et al. (2020). Geometrical data requirements in building energy modelling. *Building Data Science*, 110082.

[11] Wang, Z., et al. (2026). Weather data and micro-climatic effects in energy simulation. *Climate and Building Performance*, 113886.

[12] Wang, H., et al. (2022). Energy Performance Certificates and building assessment. *Building Certification Review*, 109056.

[13] Ang, B. W., et al. (2020). Performance metrics for building energy assessment. *Energy Management Journal*, 115738.

[14] Song, X., et al. (2025). Comparison of top-down and bottom-up energy modelling approaches. *Energy Modelling Review*, 106147.

[15] Choi, J., et al. (2024). Energy performance metrics and optimization strategies. *Building Optimization Journal*, 115042.

[16] Corgnati, S. P., et al. (2008). European Directive on Energy Performance of Buildings. *Building and Environment*, 43(5), 801–815.

[17] Bano, F., et al. (2018). Energy Performance Index as a benchmarking tool. *Sustainable Building Management*, 506.

---

**Document Type:** Research Report  
**Subject:** Urban Building Energy Modelling - Crocetta District, Turin  
**Language:** English  
**Last Updated:** December 2025
