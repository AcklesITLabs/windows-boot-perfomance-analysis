# 🔧 Windows Boot Performance Analysis

## 📌 Overview
This project analyzes Windows boot performance using Event Viewer and the Diagnostics-Performance log. The goal was to establish a true boot-time baseline and understand how Fast Startup affects system behavior.

---

## 🎯 Objective
Measure accurate boot duration and determine whether Fast Startup impacts performance readings.

---

## 🖥️ Environment
- Device: Dell Inspiron 5505  
- OS: Windows 11 Pro  
- Tools: Event Viewer, Diagnostics-Performance log  

---

## ⚙️ Process
1. Opened Event Viewer  
2. Navigated to Diagnostics-Performance → Operational log  
3. Identified Event ID 100 (boot performance)  
4. Disabled Fast Startup  
5. Restarted system  
6. Measured updated boot duration  

---

## 📊 Results
- Boot Duration: ~32.7 seconds  
- IsDegradation: false  

---

## 🐛 Issues Encountered
- Uncertainty about whether shutdown or restart produces a true boot measurement  

---

## 🔧 Resolution
- Confirmed Restart bypasses Fast Startup  
- Verified that disabling Fast Startup results in full system initialization  

---

## 💡 Key Takeaways
- Fast Startup uses hybrid shutdown and can skew boot measurements  
- Restart provides a reliable method for testing true boot performance  
- Event Viewer is a valuable tool for system performance analysis  

---

## 🚀 Future Improvements
- Analyze startup applications impact  
- Compare Defender scan timing during boot  
- Measure BIOS/UEFI initialization time  

---

## 📂 Project Files
- [Boot Performance Lab Log](logs/2026-04-19_Boot-Performance-Log.md)
