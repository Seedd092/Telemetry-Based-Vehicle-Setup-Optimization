# Telemetry-Based Vehicle Setup Optimization

Telemetry-based vehicle setup optimization project focused on reducing understeer and improving cornering performance of the Audi R8 V10, achieving ~1.9s lap time improvement.

---

## Introduction

The objective of this project is to optimize a vehicle with evident handling issues by adapting its setup to better suit both track conditions and driving style.

---

## Baseline Performance

The following analysis illustrates the vehicle’s behavior in two selected corners prior to any setup optimization. These sections were chosen as they clearly highlight the car’s handling limitations.

In both cases, the vehicle demonstrates reduced cornering efficiency, requiring increased steering input while failing to achieve the desired rotation.

### Baseline Corner Performance

| Corner | Time (s) | Exit Speed (km/h) |
|--------|--------|------------------|
| Corner 1 (Parabolic) | 11.71 | 178 |
| Corner 2 | 7.02 | 110 |

---

## Setup Changes

To address the identified understeer and improve front-end grip, a series of setup adjustments were implemented.

### Suspension & Geometry
- Front ARB: **34000 → 31000 Nm**
- Rear ARB: **10800 → 13250 Nm**
- Front track width: **1.638 → 1.668 m**
- Front toe-out: **0.00010 → 0.00310 rad (≈0.172°)**
- Front camber: **−1.4° → −3.4°**

### Differential Adjustments

**difflock_brake_mult**
- Reworked from aggressive drop-off to smoother curve:
  - (0, 0.5) → (0.10, 0.5) → (0.25, 0.2) → (0.50, 0.05) → (1, 0)

**difflock_gear_mult**
- Reduced across gears 1–7:
  ```
  Before: 13.9669 / 9.286 / 6.745 / 5.0821 / 4.0033 / 3.1696 / 2.3405  
  After:  6.5 / 5.5 / 5.0 / 4.2 / 3.6 / 3.0 / 2.3
  ```

These changes were aimed at improving front-end grip, reducing understeer, and achieving a more balanced handling characteristic.

---

## Comparison (Baseline vs Optimized Setup)

A comparison was conducted using the same two corners at Circuit de Barcelona-Catalunya.

### Key Observations

- Reduced steering input  
- Improved front-end grip  
- Transition from understeer to slight, controllable oversteer  
- Better rotation and cornering efficiency  
- Earlier throttle application on corner exit  

### Corner Performance Comparison

| Corner | Baseline Time | Optimized Time | Baseline Exit | Optimized Exit |
|--------|--------------|----------------|---------------|----------------|
| Corner 1 (Parabolic) | 11.71 s | 11.25 s | 178 km/h | 180 km/h |
| Corner 2 | 7.02 s | 7.02 s | 110 km/h | 112 km/h |

Corner 2 shows improved efficiency through increased exit speed while maintaining identical corner time.

---

## Results

Following the implemented setup changes, the Audi R8 V10 demonstrated a measurable improvement in performance.

- **Lap time:**  
  2:10.072 → 2:08.155 (**−1.9 s**)

> Note: The baseline lap included a drift-assisted section, which may have slightly influenced the result.

### Demo Video - https://youtu.be/KSa9Wp0SgqM

### Summary of Improvements

- Reduced steering input  
- Improved balance and stability  
- Increased front-end grip  
- Earlier throttle application  
- Improved corner exit speeds  

---

## Conclusion

This project demonstrates that targeted setup adjustments can significantly improve vehicle handling and performance.

By correcting the front-to-rear grip imbalance, it was possible to:
- Reduce understeer  
- Improve rotation  
- Achieve more stable and predictable cornering  

The optimized setup enabled more efficient use of available grip, resulting in improved lap time and overall driving performance.

---

## Key Takeaway

Proper setup tuning, combined with telemetry analysis, is essential for maximizing vehicle performance and adapting the car to both track conditions and driving style.
