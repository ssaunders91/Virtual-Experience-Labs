# 🛡️ Project 2: SOC Analyst Simulation (Drax)

### 🎯 Objective
The goal of this simulation was to investigate network logs flagged for anomalous activity and determine if they represented legitimate business traffic or a **Command and Control (C2) beaconing** attempt.

### 🔍 Methodology & Analysis
I employed a multi-phased approach to ensure the accuracy of the findings:

* **Initial Assessment:** Analysed traffic patterns, focusing on connection frequency (e.g., high-frequency "heartbeats" vs. "low and slow" intervals).
* **Independent Data Validation:** Conducted a second, more rigorous pass by manually verifying the reputation and ownership of all external IP addresses. 
* **Final Determination:** This secondary validation was crucial in identifying that the most "noisy" traffic was actually legitimate, while the true threat was a stealthy, low-volume connection.

### 📊 Investigation Findings

| Log | Status | Technical Reasoning |
| :--- | :--- | :--- |
| **Log A** | ✅ Safe | Routine "heartbeat" signals; verified clean IP reputation. |
| **Log B** | ⚠️ Suspicious | **Confirmed Malicious IP.** Identified as a "low and slow" beaconing attempt. |
| **Log C** | ✅ Safe | Normal cloud synchronisation behaviour from a trusted source. |
| **Log D** | ✅ Safe | Standard load-balancing across verified cloud servers. |
| **Log E** | ✅ Safe | **False Positive.** High-traffic volume from a legitimate service. |

### 💡 Key Learning
This project highlighted the importance of a **"Second Pass" investigation**. By not relying solely on automated alerts and performing manual IP reputation checks, I was able to accurately filter out false positives and pinpoint the genuine security threat.

[⬅️ Back to Virtual Work Experience Hub](https://github.com/ssaunders91/Virtual-Experience-Labs/blob/main/README.md)

[⬅️ Back to Profile Hub](https://github.com/ssaunders91)
