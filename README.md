# VCRS-Modelling
Inter IIT Tech Meet 13.0 -- Vapor Compression Cycle Modelling


📘 Project Overview

A detailed VCAC system was developed based on the thermodynamic vapor compression cycle. It includes component selection, refrigerant analysis, simulation modeling, and performance evaluation.

1. 🔍 Introduction

The system is designed to maintain indoor thermal comfort efficiently. It comprises a single compressor and uses thermodynamic models for temperature and humidity regulation.

2. 🧰 Model Design

Simulink and Simscape Fluids were used to construct and simulate the VCAC system.

Key components include the compressor, condenser, expansion valve, and evaporator.

Controllers and sensors manage temperature and pressure regulation.

3. 🧪 Refrigerant Selection

Several refrigerants were compared based on COP, GWP, ODP, flammability, and toxicity.
R1234yf was finalized due to its balanced performance and environmental safety.

4. ⚙️ Component Overview

Compressor

Scroll Compressor 2 was selected for compatibility with R1234yf.

Condenser

Designed for efficient heat rejection using a coiled tube configuration and optimized fin area.

Expansion Valve

Thermostatic type modeled based on nominal and peak mass flow conditions.

Evaporator

Designed to maximize heat absorption using a 40m coiled tube and optimized surface area.

5. 🎛️ Control Logic

A PI controller was implemented to maintain the desired indoor temperature by adjusting the speeds of the compressor, indoor fan, and outdoor fan.

Kp (Proportional Gain): Fixed at 1

Ki (Integral Gain): Scheduled based on the desired temperature using gain scheduling

Benefits of using a gain scheduling PI controller is as follows .

Eliminates steady-state error

Improves control precision

Enhances dynamic adaptability

Ensures system stability

Boosts energy efficiency

6. 📈 Performance Metrics

ISEER (Indian Seasonal Energy Efficiency Ratio)

Cooling capacity and power input were calculated across seasonal temperature bins.

ISEER = 3.385

EER (Energy Efficiency Ratio)

EER Formula: EER = Cooling Capacity (Btu/hr) / Power Input (Watts)

Cooling capacity calculated using Q = M(h1 - h4)

Average EER = ISEER × 3.412 = 11.55

7. ✅ Testing Conditions

Performance was evaluated using standardized ISEER conditions:

Outdoor Temperature: 35°C

Indoor Dry Bulb Set Point: 27°C

Indoor Wet Bulb Set Point: 19°C
