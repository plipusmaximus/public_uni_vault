---
dg-publish: true
---
# Power Berechnung
**3 Phasen:** 
Apparent Power $S_{L}=\sqrt{ 3 }U_{LN}I_{LN}$
Active Power $P_{L}= \sqrt{ 3 } U_{L N} \prescript{1}{}{I}_{LN} \cos(\varphi_{1})$ 
Reactive Power of the fundamental component: $\prescript{1}{}{Q}_{L}= \sqrt{ 3 } U_{L N} \prescript{1}{}{I}_{LN} \sin(\varphi_{1})$
Distortion Power: $D_{L}=\sqrt{ S_{L}^{2} - P_{L}^{2} - \prescript{1}{}{Q}_{L}^{2} }$
Total reactive Power: $Q_{L}=\sqrt{\prescript{1}{}{Q}_{L}^{2}+D_{L}^{2}  }$
# DC-DC Converter
## Galvanically non-isolated Converters
### Buck Converter
![[file-20260310141533091.png]]
S turned on:
![[file-20260310141631060.png]]
S turned off:
![[file-20260310141702989.png]]
CCM: $U_{out}=dU_{in}$ und $\bar{I}_{in}=d \bar{I}_{out}$ da $\bar{P}_{in}=\bar{P}_{out}$ und $\Delta I_{out} = \frac{U_{out}}{L}(1-d)T$ 
### Boost Converter
![[file-20260310141749131.png]]
S turned on:

S turned off:

### Buck-Boost Converter
![[file-20260310141824843.png]]
$U_{out}=\frac{d}{1-d}U_{in}$ 
$\Rightarrow$ When booth switches are operated with same duty cycle d
![[file-20260310141913682.png]]
!! ==Output voltage changed sign== !!
### Two Quadrant Converters
#### Synchronus Buck Converter
![[file-20260310142042437.png]]
![[file-20260310142058000.png]]
![[file-20260310142118877.png]]
- 1. Quadrant: Buck Converter mit $S_{1}$ und $D_{2}$
- 4. Quadrant: "Boost" Converter mit $S_{2}$ und $D_{1}$ 
	- Umgedrehter Boost mit $U_{out}$ als $\bar{U}_{in}$ des Boost-Converters $\Rightarrow$ Spannung $U_{out}\leq U_{in}$ 
#### Half-Bridge-DC-DC Converter
![[file-20260310142748345.png]]
- $S_{4}$ permanently on $\Rightarrow$ Buck Converter
- $S_{1}$ permanently off $\Rightarrow$ "Boost" Converter with changed sign$\Rightarrow$ $U_{out}\leq 0$ 
- ![[file-20260310143059322.png]]
### Full-Bridge-DC-DC/Four-Quadrant Converter
Alles Mosfets also Switch plus Diode
![[file-20260310143248249.png]]
## Galvanically isolated Converters
### Flyback Converter
![[file-20260310143943722.png]]
$E=\frac{\hat{I}_{prim}^{2}L_{m}}{2}=\frac{U_{in}^{2}d^{2}}{2 f_{sw}^{2} L_{m}}$ $\Rightarrow$ $d=\frac{\sqrt{ 2f_{sw}L_{m}P_{out} }}{U_{in}}=\frac{\sqrt{ 2f_{sw}L_{m}U_{out}I_{out}}}{U_{in}}$
### Foreward Converter
![[file-20260310144005145.png]]
- limited Buck-Converter with $U_{out}=U_{in} \frac{N_{2}}{N_{1}}d$ and $d=\frac{1}{1+\frac{N_{3}}{N_{1}}}$ with $d_{max}=\frac{1}{1+1}=\frac{1}{2}$ 
- $N_{3}$ used for demagnetization 
### Push-Pull Converter
![[file-20260310144019167.png]]
- limited Buck-Converter with $U_{out}=U_{in} \frac{N_{2}}{N_{1}}d$ 
- better usage of the (expensive) magnetic components than with [[Klausurzusammenfassung#Foreward Converter|Foreward Converter]]  
- full duty cycle possible again
- $S_{1}$ and $S_{2}$ operated with same duty cycle $d$ shifted by $\frac{T}{2}$ 
- Problem: small asymmetry in switching times leads to gradual magnetization $\Rightarrow$ monitoring necessary
### Half-Bridge Converter
![[file-20260310144033923.png]]
- Voltage divider $C_{1}$ and $C_{2}$ leads to $\pm \frac{U_{in}}{2}$ being transformed to the other site
- $U_{out}=\frac{U_{in}}{2} \frac{N_{2}}{N_{1}} d$ 
### Full-Bridge Converter
![[file-20260310144045890.png]]
- $U_{out}=U_{in}\frac{N_{2}}{N_{1}} d$ 
- pairwise conduction of $S_{1}$ and $S_{4}$ or $S_{2}$ and $S_{3}$  
### Single-Active-Bridge Converter
Smoothing Inductance $L$ is included in the 
### Dual-Active-Bridge Converter 
#### 1DAB
![[file-20260310144231841.png]]
#### 3DAB
![[file-20260310144328305.png]]

# Hystheresis
$\frac{d i_{out}}{dt}=\frac{u_{L}}{L}$ Steigung in den einzelnen Schaltzuständen bla
# Space Vector Modulation
$\begin{pmatrix}x_{\alpha} \\ x_{\beta}\end{pmatrix}=\begin{pmatrix} \frac{2}{3} & -\frac{1}{3} & -\frac{1}{3} \\ 0 & \frac{1}{\sqrt{ 3 }} & -\frac{1}{\sqrt{ 3 }}\end{pmatrix} \begin{pmatrix}x_{1} \\ x_{2} \\ x_{3}\end{pmatrix}$ 
$\begin{pmatrix}x_{1} \\ x_{2} \\ x_{3}\end{pmatrix}=\begin{pmatrix}1 & 0 \\ -\frac{1}{2} & \frac{\sqrt{ 3 }}{2} \\ -\frac{1}{2} & -\frac{\sqrt{ 3 }}{2}\end{pmatrix}\begin{pmatrix}x_{\alpha} \\ x_{\beta}\end{pmatrix}$ 
# ==Inverter== 
