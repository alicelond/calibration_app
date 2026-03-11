# Microphone Sensitivity Analysis Tool

This is a personal project focused on practising the structure of MATLAB App Designer. 

## 🎯 Overview
The AudioCalibrator allows acoustic engineers to determine the sensitivity of measurement microphones by analysing signals from standard acoustic calibrators (IEC 60942). The app processes `.wav` recordings, calculates physical units, and exports calibration factors for offline use.

---

## 📋 Software Requirements Specification

### 1. Functional Requirements (FR)
| ID | Requirement | Description |
|:---|:---|:---|
| **FR01** | **File Selection** | The system shall allow the user to browse and select a `.wav` file via a standard UI file explorer. |
| **FR02** | **Reference Input** | The system shall allow manual input of Reference SPL (dB) and Reference Frequency (Hz). |
| **FR03** | **Waveform Plot** | The system shall render the time-domain signal (Voltage vs. Time) immediately upon loading. |
| **FR04** | **Sensitivity Calculation** | The system shall compute the RMS voltage and derive the sensitivity in $mV/Pa$. |
| **FR05** | **Stability Check** | The system shall validate signal stability (variance check) before finalising the result. |
| **FR06** | **Data Export** | The system shall export the results (factor, date, metadata) to `.mat` or `.json` formats. |

### 2. Non-Functional Requirements (NFR)
* **NFR01 - Standalone Execution:** The app must be compiled into a `.exe` using the **MATLAB Compiler**, running offline via **MATLAB Runtime**.
* **NFR02 - Event-Driven Architecture:** All logic must be triggered by UI Callbacks (e.g., `ButtonPushedFcn`).
* **NFR03 - Modern UI:** Developed using **MATLAB App Designer** (Class-based structure).
* **NFR04 - Error Handling:** Implementation of `try-catch` blocks for file I/O and `uialert` for user notifications.
* **NFR05 - Metrological Compliance:** Logic follows **IEC 61094** guidelines for microphone calibration.

---

## 🏗️ Technical Stack
* **Language:** MATLAB
* **Framework:** App Designer (Uifigure)
* **Toolboxes:** Audio Toolbox, MATLAB Compiler
* **Version Control:** Git / GitHub

---

## 🛠️ Implementation Strategy
1. **Figma Prototyping:** UX/UI layout design.
2. **Core Logic:** Developing standalone functions for RMS and dB-to-Pascal conversion.
3. **App Integration:** Binding logic to UI components via Callbacks.
4. **Build:** Compiling the standalone executable for production use.
