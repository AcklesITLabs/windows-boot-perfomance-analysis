# 🧪 Windows Boot Performance Analysis

> A structured analysis of Windows boot performance using native system tools and event logging.

---

## 📚 Table of Contents
- Summary
- Objective
- Environment
- Methodology
- Results
- Challenge
- Resolution
- Key Takeaways
- Next Steps
- Conclusion

---

## 📌 Summary
This project analyzes Windows boot performance using Event Viewer and the Diagnostics-Performance log. The goal was to establish a true boot-time baseline and understand how Fast Startup affects system behavior.

---

## 🎯 Objective
Establish a reliable baseline for Windows boot performance and evaluate the impact of Fast Startup on measured boot times.

---

## 🖥️ Environment
- Device: Dell Inspiron 5505  
- OS: Windows 11 Pro  
- Tools: Event Viewer, Diagnostics-Performance log  

---

## ⚙️ Methodology
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

## 🐛 Challenge
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

## 🚀 Next Steps
- Analyze startup applications impact  
- Compare Defender scan timing during boot  
- Measure BIOS/UEFI initialization time  

---

## 📌 Conclusion

This analysis demonstrates how built-in Windows tools can be used to accurately measure and interpret system boot performance. Disabling Fast Startup provides a more reliable baseline for true system initialization behavior.

---

## 📂 Project Files
- [Boot Performance Lab Log](logs/2026-04-19_Boot-Performance-Log.md)
