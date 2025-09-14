This repository presents a concise overview of the modeling and optimization of a Vapor Compression Air Conditioning (VCAC) system using MATLAB/Simulink. The project focuses on achieving energy-efficient cooling and dehumidification under various operational conditions.

<img width="687" height="363" alt="image" src="https://github.com/user-attachments/assets/6f79cd23-d8dc-4853-9d80-cb574ec6d490" />

📘 Project Overview

A detailed VCAC system was developed based on the thermodynamic vapor compression cycle. It includes component selection, refrigerant analysis, simulation modeling, and performance evaluation.

1. 🔍 Introduction

The VCAC system was designed to maintain indoor thermal comfort in an energy-efficient manner. It employs a single compressor and relies on thermodynamic models to regulate both temperature and humidity levels. The primary goal of the system was to ensure optimal cooling performance under varying environmental conditions while keeping energy consumption low.

2. 🧰 Model Design

The VCAC system was modeled and simulated using MATLAB/Simulink with the Simscape Fluids library. The simulation incorporates key thermodynamic components, including a compressor, condenser, expansion valve, and evaporator. Control systems and sensors were implemented to monitor and regulate temperature and pressure. This setup facilitated a realistic representation of system dynamics and control response.

3. 🧪 Refrigerant Selection

Several refrigerants were evaluated based on parameters such as coefficient of performance (COP), global warming potential (GWP), ozone depletion potential (ODP), flammability, and toxicity. After comparison, R1234yf was selected as the refrigerant due to its favorable balance between performance and environmental safety. It provides efficient cooling while minimizing environmental impact.

4. ⚙️ Component Overview

The system employs Scroll Compressor 2, which is compatible with the chosen refrigerant, R1234yf. The condenser was designed using a coiled tube configuration with optimized fin area to ensure effective heat rejection. A thermostatic expansion valve was modeled to handle both nominal and peak mass flow conditions, allowing for stable pressure control. The evaporator, constructed with a 40-meter coiled tube and enhanced surface area, ensures efficient heat absorption from the indoor environment.

5. 🎛️ Control Logic

A Proportional-Integral (PI) controller was developed to regulate the indoor temperature by adjusting the speeds of the compressor, indoor fan, and outdoor fan. The proportional gain (Kp) was fixed at 1, while the integral gain (Ki) was scheduled based on the target temperature using a gain scheduling method. This approach enhances system responsiveness and stability.

To implement gain scheduling, a lookup table was defined with breakpoints at specific temperature values [17, 19, 21, 23, 25, 27, 29] °C and corresponding Ki values [0.00004, 0.00005, 0.000064, 0.00009, 0.00014, 0.00030, 0.0004]. Linear interpolation between these points allows for smooth transitions in controller behavior. This configuration helps eliminate steady-state errors, improve precision, enable adaptability to varying loads, ensure stable system response, and promote energy efficiency.

6. 📈 Performance Metrics

The performance of the system was evaluated using the Indian Seasonal Energy Efficiency Ratio (ISEER), which accounts for seasonal variations in temperature. Cooling capacity and power input were calculated across standard temperature bins, resulting in an ISEER value of 3.385.

In addition to ISEER, the Energy Efficiency Ratio (EER) was assessed. EER is defined as the ratio of cooling capacity (in Btu/hr) to power input (in Watts). Cooling capacity was calculated using the formula Q = M(h1 - h4), where M is the mass flow rate and h1, h4 are the enthalpies across the evaporator. Converting Q to Btu/hr and applying the EER formula yielded an average EER of 11.55, using the relation EER = ISEER × 3.412.

7. ✅ Testing Conditions

System performance was validated under standardized ISEER test conditions. These included an outdoor temperature of 35°C, an indoor dry bulb set point of 27°C, and an indoor wet bulb set point of 19°C. These conditions simulate realistic operational scenarios and help benchmark system efficiency and control accuracy. 
