# Wind Turbine Gearbox FMEA (Failure Mode and Effects Analysis)

## Executive Summary
This case study investigates critical gearbox and drivetrain failure modes in a commercial wind turbine. Root-cause analysis indicates that **over-lubrication** serves as the primary system driver, leading to seal failures, oil migration onto brake surfaces, and subsequent bearing vibration.

## FMEA Quantification Matrix

| Failure Mode | Cause | Severity (S) | Occurrence (O) | Detection (D) | RPN | Recommended Actions |
| :--- | :--- | :---: | :---: | :---: | :---: | :--- |
| **High gearbox temp alarms** | Radiator/Cooling system hardware failure | 9 | 7 | 8 | **504** | Inspect heat exchanger coil, verify coolant pump operation, and clean intake blockage. |
| **Gearbox oil leaks** | Damaged oil seals due to over-lubrication | 10 | 5 | 2 | **100** | Verify overflow via SCADA telemetry; replace damaged seals and enforce strict fill-level caps. |
| **Bearing vibration above limit** | Shaft or coupling misalignment | 10 | 4 | 7 | **280** | Perform laser shaft alignment and re-torque coupling bolts during scheduled shutdown. |
| **Generator trips unexpectedly** | Overheating due to short circuit or electrical fault | 10 | 3 | 4 | **120** | Pull SCADA fault code logs to isolate whether trip was preceded by overcurrent or excess vibration. |
| **Brake fails functional test** | Oil migration onto brake pads from over-lubrication | 8 | 2 | 3 | **48** | Visually inspect disc/pads; replace contaminated friction pads and degrease brake rotor. |
| **Temp sensor false alarms** | Mechanical vibration transfer from bearing/shaft | 9 | 3 | 5 | **135** | Inspect sensor mounting housing and install vibration-damping isolation mounts. |

---

## Root Cause Analysis & Systemic Impact
Physical inspection and maintenance logs indicate that **excessive manual lubrication** caused pressure buildup within seal cavities. Oil escaped into the Nacelle floor and migrated onto mechanical brake assemblies, reducing friction efficiency and creating secondary operational hazards.

### Immediate Mitigation Protocol
* **Emergency Stop:** Halt turbine operation immediately upon high temperature or oil migration detection to prevent catastrophic gearbox seizure.
* **SCADA Telemetry Integration:** Deploy real-time oil level and particle-count sensors to trigger automated warnings prior to manual overflow.
* **Predictive Maintenance:** Implement oil health scoring to schedule oil changes strictly during low-wind periods.

---

## Downtime Cost & Engineering Decision Analysis

### Financial Impact Breakdown
* **Downtime Rate:** $4,000 / day
* **Bearing Replacement Hardware:** $80,000.
* **Average Repair Timeline:** 5 days ($20,000 downtime loss)
* **Total Financial Impact per Occurrence:** **$100,000**

### Engineering Trade-Off: Bearing vs. Full Gearbox Replacement
While replacing only the damaged bearings costs less upfront, previous critical stress cycles likely induced subsurface micro-cracks across adjacent gears and shafts.

**Recommendation:** Perform a **Full Gearbox Replacement** combined with complete oil sump flushing, provided housing integrity is verified. This eliminates latent fatigue failure risks and extends system operating life beyond 5 years.
