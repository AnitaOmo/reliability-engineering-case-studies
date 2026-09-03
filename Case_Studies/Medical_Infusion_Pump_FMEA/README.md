# Medical Infusion Pump FMEA (Failure Mode and Effects Analysis)

## Overview
This case study evaluates the primary physical and mechanical failure modes of a medical infusion pump. The analysis prioritizes operational risks, quantifies Risk Priority Numbers (RPN), and outlines targeted corrective actions based on historical maintenance data and regulatory guidance.

## FMEA Matrix

| Process / Item | Failure Mode | Cause | Severity (S) | Occurrence (O) | Detection (D) | RPN | Recommended Actions |
| :--- | :--- | :--- | :---: | :---: | :---: | :---: | :--- |
| **Medical Infusion Pump** | Battery no longer holds charge | Normal Wear (gradual degradation due to repeated charging) | 8 | 9 | 2 | **144** | Add an alarm sensor to notify staff after a full charge and at 25% battery level to discourage overcharging and ensure continuous operation. |
| **Medical Infusion Pump** | Touchscreen becomes unresponsive | Human Error / Chemical Damage (fails to register input or locks up after disinfectant cleaning) | 7 | 9 | 3 | **189** | Train staff to wipe down the touchscreen with a dry, tight-weave microfiber cloth after disinfecting and before inputting values. |
| **Medical Infusion Pump** | Flow rate sensor drifts out of calibration | Mechanical Wear (leads to inaccurate medication dosage) | 9 | 8 | 8 | **576** | Schedule routine preventive maintenance checks; analyze drift data prior to adjustment and verify calibration accuracy every 6 months. |
| **Medical Infusion Pump** | Power Supply Failure | Battery degradation and failure of battery backup system (causes sudden unit shutdown) | 9 | 1 | 8 | **72** | Implement telemetry/sensors that alert when backup battery issues occur, or deploy software monitoring battery health. |
| **Medical Infusion Pump** | Alarm Speaker Failure | Hardware failure, software error, or setting configuration (pump operates but alarm is silent) | 8 | 8 | 7 | **448** | Verify volume levels, run software diagnostics to isolate electrical vs. mechanical faults, and immediately swap with a functional unit while repairing. |
| **Medical Infusion Pump** | Housing Cracks | Accidental physical impact, tubing misalignment stress, or harsh cleaning chemical degradation | 8 | 9 | 7 | **441** | Remove and replace immediately per FDA guidelines to prevent fluid ingress or dosage risks to patients. |

## Key Insights & Action Items
* **Critical Focus Area:** Flow Rate Sensor Drift ($\text{RPN} = 576$) represents the highest clinical risk due to potential medication dosage inaccuracies.
* **Secondary Risk:** Alarm Speaker Failure ($\text{RPN} = 448$) requires immediate isolation protocol because silent operation bypasses primary clinical alerts.
* **Data Sources:** Detection ratings and occurrence frequencies were validated against historical maintenance logs and FDA safety advisories.
