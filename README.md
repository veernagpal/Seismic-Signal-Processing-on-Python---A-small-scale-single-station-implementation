# Seismic Wave Processing using Python

## Table of Contents

* Overview
* Features
* Technologies Used
* How It Works
* Setup & Run
* Output

---

## Overview

This project is a simple Python script that simulates how earthquake signals are processed.

It generates a synthetic seismic signal, removes noise, detects **P-waves** and **S-waves**, and estimates:

* Distance to the earthquake
* Approximate magnitude (Richter scale)

The goal is to demonstrate basic **digital signal processing (DSP)** concepts used in seismology in a simple and understandable way.

---

## Features

* Synthetic seismic signal generation (noise + P-wave + S-wave)
* Bandpass filtering to clean the signal
* Automatic wave detection using STA/LTA algorithm
* Distance estimation using P–S time difference
* Magnitude estimation (approximate)
* Visualization of:

  * Continuous waveform
  * Filtered signal with detected waves
  * STA/LTA ratio

---

## Technologies Used

* **Python**
* **NumPy** – numerical computations and signal generation
* **SciPy** – signal filtering (Butterworth filter)
* **Matplotlib** – plotting graphs and visualization

---

## How It Works

1. Generate a fake seismic signal (noise + waves)
2. Apply a bandpass filter (0.5–10 Hz) to remove noise
3. Compute STA/LTA ratio to detect wave arrivals
4. Identify:

   * First spike → P-wave
   * Second spike → S-wave
5. Calculate:

   * Distance using time difference
   * Magnitude using amplitude

---

## Setup & Run

### 1. Create virtual environment

```bash
python -m venv venv
```

### 2. Activate it

**Linux:**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install numpy matplotlib scipy
```

### 4. Run the script

```bash
python your_script_name.py
```

---

## Output

* Console prints:

  * Detected P-wave time
  * Detected S-wave time
  * Estimated distance
  * Estimated magnitude

* Graphs:

  * Continuous seismic waveform
  * Filtered signal with detections
  * STA/LTA ratio plot

