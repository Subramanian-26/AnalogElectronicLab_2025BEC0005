# AnalogElectronicLab
# Experiment-01: NMOS Characterization

## Aim

To characterize an NMOS transistor using **Cadence Virtuoso and Spectre** by obtaining its:

* (I_D)–(V_{GS}) transfer characteristic
* (I_D)–(V_{DS}) output characteristics for different (V_{GS}) values
* DC operating-point parameters

---

## Design Specifications

| Parameter       |                      Value |
| --------------- | -------------------------: |
| NMOS Model      |                   `nmos1v` |
| Technology      |                  `gpdk090` |
| Width (W)       |                       1 µm |
| Length (L)      |                     100 nm |
| (V_{GS}) Sweep  |                0 V – 1.2 V |
| (V_{DS}) Sweep  |                0 V – 1.2 V |
| Simulation Tool | Cadence Virtuoso / Spectre |

The NMOS used in the schematic is from the `gpdk090` library and is configured with **W = 1 µm** and **L = 100 nm**.

---

## Circuit Description

The NMOS transistor is configured for DC characterization.

* The **source** terminal is connected to ground.
* A DC voltage source `V2` is connected to the **gate** and is defined as `VGS`.
* A DC voltage source `V0` is connected to the **drain** and is defined as `VDS`.
* The drain current is observed as the primary output.
* The body/source reference is connected to ground.

## Simulation Procedure

### 1. Schematic Creation

The NMOS characterization circuit was created in **Cadence Virtuoso Schematic Editor** using the `nmos1v` device from the `gpdk090` library.

The transistor dimensions were set to:

* **W = 1 µm**
* **L = 100 nm**

Two DC voltage sources were used:

* `VGS` for gate-source voltage
* `VDS` for drain-source voltage

---

### 2. VGS Sweep

A DC analysis was configured to study the variation of drain current with gate-source voltage.

The design variable `VGS` was swept from:

**0 V → 1.2 V**


The drain current was selected as the output quantity.

---

### 3. Obtaining the VGS Characteristic

After running the simulation, the drain current was plotted against `VGS`.

The resulting characteristic shows that the drain current remains very small at lower values of (V_{GS}) and increases significantly as (V_{GS}) increases.



---

### 4. VDS Parametric Sweep

For obtaining the output characteristics, (V_{DS}) was swept from:

**0 V → 1.2 V**

The simulation was performed for multiple values of (V_{GS}).

The resulting curves show the variation of drain current (I_D) with drain-source voltage (V_{DS}) for different gate-source voltages.


---

### 5. DC Operating Point Analysis

A DC operating-point analysis was performed using Cadence ADE.

The operating-point parameters of the NMOS were obtained from the Spectre simulation.



For the displayed operating point:

* (V_{GS} = 1,V)
* (V_{DS} = 0.6,V)
* (V_{BS} \approx 0,V)
* (V_{TH} \approx 211.47,mV)

The operating-point window also provides other device parameters such as `vdsat`, `gm`, `ron`, and related transistor quantities.



---

## Results

### VGS Transfer Characteristic

The simulated (I_D)–(V_{GS}) characteristic shows that:

* Drain current is almost zero at low (V_{GS}).
* Drain current begins increasing significantly as (V_{GS}) approaches the threshold region.
* Drain current increases rapidly with further increase in (V_{GS}).

From the displayed operating-point data, the threshold voltage is approximately:

[
\boxed{V_{TH} \approx 211.47,mV}
]

---

### VDS Output Characteristics

The (I_D)–(V_{DS}) characteristics were obtained for different values of (V_{GS}).

The graph shows:

* Higher (V_{GS}) produces higher drain current.
* At lower (V_{DS}), the drain current increases more rapidly.
* At higher (V_{DS}), the curves become comparatively less steep.

---

### DC Operating Point

For the displayed operating point:

| Parameter  | Simulated Value |
| ---------- | --------------: |
| (V_{GS})   |             1 V |
| (V_{DS})   |           0.6 V |
| (V_{BS})   |           ≈ 0 V |
| (V_{TH})   |     ≈ 211.47 mV |
| (V_{DSAT}) |     ≈ 402.10 mV |

---

## Observations

1. The NMOS remains nearly off for low values of (V_{GS}).
2. Drain current increases significantly once (V_{GS}) exceeds the threshold region.
3. Increasing (V_{GS}) increases the drain current for a given (V_{DS}).
4. The (I_D)-(V_{DS}) curves demonstrate the different operating regions of the NMOS.
5. The simulated threshold voltage obtained from the operating-point analysis is approximately **211.47 mV**.
6. For the displayed operating point, (V_{DS}=0.6,V) and (V_{GS}=1,V).

---

## Conclusion

The NMOS transistor was successfully characterized using **Cadence Virtuoso/Spectre**.

The (I_D)-(V_{GS}) and (I_D)-(V_{DS}) characteristics were obtained through DC and parametric sweep analyses. The simulation demonstrates the dependence of drain current on gate-source and drain-source voltages. The DC operating-point analysis also provided important NMOS parameters, including a threshold voltage of approximately **211.47 mV** for the displayed operating point.

---

### GitHub Repository

**Analog Electronics Lab — 2025BEC0005**

`https://github.com/Subramanian-26/AnalogElectronicLab_2025BEC0005`

**Student:** Subramanian R
**Roll No.:** 2025BEC0005

