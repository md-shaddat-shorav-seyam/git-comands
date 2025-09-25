Got it — I solved every question from your uploaded worksheet step-by-step. The problems I used are from your PDF. 

Below are clear, numbered solutions (showing assumptions and every arithmetic step).


---

Boiler / Steam Generator — Problem 1

Given: steam enthalpy , feed water enthalpy , steam rate , latent heat .

1. Heat required per kg steam (enthalpy rise)



\Delta h = h_s - h_f = 2620 - 270 = 2350\ \text{kJ/kg}.

2. Steam generation factor (equivalent evaporation factor) — taken as



\text{factor} = \frac{\Delta h}{L} = \frac{2350}{2257}=1.0412\ (\text{dimensionless}).

3. Heat duty per hour:



Q_{\text{hr}} = \dot m \cdot \Delta h = 50\times 2350 = 117500\ \text{kJ/hr}.

4. Convert to kW: , and 1 hr = 3600 s



P = \frac{117500}{3600} = 32.6389\ \text{kW}.

Answers: Steam generation factor . Boiler power .


---

Boiler — Problem 2

Given: feed water , coal burned , net enthalpy rise per kg water , calorific value CV .

1. Heat absorbed by water per hour:



Q_{\text{absorbed}} = 205\times 145 = 29725\ \text{kJ/hr}.

2. Fuel energy input per hour:



Q_{\text{fuel}} = 23\times 2050 = 47150\ \text{kJ/hr}.

3. Boiler efficiency:



\eta = \frac{Q_{\text{absorbed}}}{Q_{\text{fuel}}}\times 100\% = \frac{29725}{47150}\times 100\% = 63.04\%.

Answer: Boiler efficiency ≈ 63.04%.


---

Boiler — Problem 3 (chimney height)

Given: boiler uses ; required draught ; mean chimney gas temp ; outside air .

We use the standard textbook relation for natural draft (mm water):

h_w = 353\,H\left(\frac{1}{T_a} - \frac{M_a+1}{M_a\,T_g}\right)

1. Convert temps:



T_a = 27+273 = 300\ \text{K},\quad T_g=315+273=588\ \text{K}.

2. Rearranged for :



H = \frac{h_w}{353\left(\dfrac{1}{T_a} - \dfrac{M_a+1}{M_a\,T_g}\right)}.

3. Substitute numbers:



\frac{1}{T_a} = \frac{1}{300}=0.00333333,\quad
   \frac{M_a+1}{M_a\,T_g}=\frac{19}{18\times 588}=0.00179598.

Then

H=\frac{25}{353\times 0.00153735}=46.04\ \text{m}.

Answer: Minimum chimney height ≈ 46.04 m.


---

Boiler — Problem 4 (air used per kg fuel from given chimney data)

Given: chimney height ; draught ; , boiler-house (ambient) ; atmospheric pressure given but not needed in the standard formula.

Use the same textbook formula:

h_w = 353\,H\left(\frac{1}{T_a} - \frac{M_a+1}{M_a\,T_g}\right)

A \equiv \frac{1}{T_a} - \frac{h_w}{353H} = \frac{M_a+1}{M_a\,T_g}

\frac{1}{M_a} = T_g A - 1 \quad\Rightarrow\quad M_a = \frac{1}{T_g A - 1}.

1. Convert temps: 


2. Compute



\frac{h_w}{353H}=\frac{16.5}{353\times 30}=0.0016248, \quad \frac{1}{T_a}=0.00332226.

3. Then



M_a = \frac{1}{633\times 0.00169746 - 1} = \frac{1}{1.0747 - 1} = \frac{1}{0.0747} = 8.5668\ \text{kg air/kg fuel}.

Answer: Quantity of air ≈ 8.57 kg air per kg fuel.

(derivation & formula reference as above). 


---

IC Engine — Problem 1 (Otto / constant-volume) — parts A,B,C

Given: single-cylinder two-stroke, bore , stroke , clearance volume . Engine speed . Indicated mean effective pressure . Fuel consumption  with calorific value . Use  for air.

A. Air-standard (Otto) efficiency

1. Swept (displaced) volume:



V_s = \frac{\pi}{4}d^2L = \frac{\pi}{4}(0.2)^2(0.3)=0.00942478\ \text{m}^3.

2. Compression ratio:



r=\frac{V_s+V_c}{V_c}=\frac{0.00942478+0.00278}{0.00278}=4.39021.

3. Otto cycle (air-standard) efficiency:



\eta_{\text{otto}} = 1 - \frac{1}{r^{\gamma-1}} = 1 - \frac{1}{4.39021^{0.4}} = 0.44664 = 44.66\%.

B. Indicated power developed

Work per cycle ≈ . For a two-stroke engine there is one power stroke per revolution, so cycles per second .

P_{\text{ind}} = p_m \, V_s \times \frac{N}{60}
= (5.2\times10^5)\times 0.00942478 \times \frac{135}{60}

P_{\text{ind}} = 11026.99\ \text{W} = 11.027\ \text{kW}. 

C. Indicated thermal efficiency

1. Fuel energy input (kW):



\dot V_{\text{fuel}} = 8.8\ \text{m}^3/\text{hr} = \frac{8.8}{3600}\ \text{m}^3/\text{s}.

P_{\text{fuel}} = \frac{8.8\times 16350}{3600} = 39.9667\ \text{kW}.

2. Indicated thermal efficiency:



\eta_{\text{th,ind}} = \frac{P_{\text{ind}}}{P_{\text{fuel}}} = \frac{11.02699}{39.9667}=0.27590 = 27.59\%.

Answers (Problem 1 IC):

(A) Air-standard (Otto) efficiency ≈ 44.66%. 

(B) Indicated power ≈ 11.03 kW.

(C) Indicated thermal efficiency ≈ 27.59%.



---

IC Engine — Problem 2

Same geometry as above (d=200 mm, stroke=300 mm,  L). Air standard efficiency is the same as computed in previous problem:

Answer: . 


---

IC Engine — Problem 3 (Diesel cycle)

Given: compression ratio , cutoff ratio (fuel cut-off) . Take .

Air-standard efficiency of Diesel cycle (cold-air-standard) is

\eta_{\text{diesel}} = 1 - \frac{1}{r^{\gamma-1}}\cdot\frac{\rho^\gamma - 1}{\gamma(\rho - 1)}.

Substitute:

\eta_{\text{diesel}} = 1 - \frac{1}{13^{0.4}}\cdot\frac{1.96^{1.4}-1}{1.4(1.96-1)}.

\eta_{\text{diesel}} \approx 0.58250 = 58.25\%.

Answer: Diesel (air-standard) efficiency ≈ 58.25%. 


---

Final summary of numerical answers (rounded)

Boiler 1: steam generation factor = 1.0412; boiler power = 32.64 kW. 

Boiler 2: efficiency = 63.04%. 

Boiler 3: chimney height ≈ 46.04 m.  

Boiler 4: air per kg fuel ≈ 8.57 kg/kg fuel.  

IC 1: Otto air-standard η ≈ 44.66%; indicated power ≈ 11.03 kW; indicated thermal η ≈ 27.59%.  

IC 2: Otto air-standard η ≈ 44.66%.  

IC 3: Diesel air-standard η ≈ 58.25%.  



---

If you want, I can:

show the same solutions but with every algebra step typeset as LaTeX for printing, or

produce a clean PDF/Word with these step-by-step solutions, or

re-solve using slightly different assumptions (e.g., use 300.15 K vs 300 K for ambient) and show sensitivity.


Which (if any) would you like next?

