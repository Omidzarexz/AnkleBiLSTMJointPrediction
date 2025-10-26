# AnkleBiLSTMJointPrediction  
Predicting ankle-joint trajectories during gait using dual IMU sensors & a Bi-LSTM network  

---

## 🚀 Overview  
This repository hosts the code and dataset accompanying our research into ankle joint angle prediction using wearable inertial measurement units (IMUs) and deep learning. We apply a bidirectional long short-term memory (Bi-LSTM) network to estimate ankle joint trajectories given two IMU sensor streams, with the goal of enabling motion-aware rehabilitation robotics and personalized exoskeleton control without heavy per-user calibration.

---

## 📌 Key Features  
- **Dual IMU configuration**: Two sensors (mounted on shank and foot) supply raw accelerometer + gyroscope signals, plus complementary-filter derived orientation features.  
- **Multi-horizon prediction**: Our model supports short-term (~200 ms; 20 time-steps) and medium-term (~500 ms; 50 time-steps) forecast horizons.  
- **Evaluation paradigms**:  
  - *Cross-subject* (train on 5 subjects, test on 1)  
  - *Within-subject* (80/20 split per subject)  
  - *Transfer learning* (pre-train on 5 subjects, fine-tune on a new subject)  
- **Complete pipeline**: From raw data acquisition → preprocessing → model training → evaluation.  
- **Results (select highlights)**:  
  - Cross-subject (50-step horizon): ~3.57° MAE  
  - Within-subject: ~1.15° MAE  
  - Transfer learning: ~1.08° MAE (near within-subject performance with minimal user-specific data)  
  > *These results demonstrate the potential to significantly reduce calibration effort in rehabilitation robotics and prosthesis/exoskeleton applications.*

---

