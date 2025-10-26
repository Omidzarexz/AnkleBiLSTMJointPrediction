This repository contains the code and dataset for our research on predicting ankle joint trajectories during gait using dual IMU sensors and deep learning techniques.



📄 Overview
This project implements a bidirectional long short-term memory (Bi-LSTM) network to predict ankle joint angles using data from two wearable IMU sensors (mounted on shank and foot). The system was validated against optical encoder ground truth measurements and demonstrates high accuracy in predicting both short-term (200ms) and medium-term (500ms) ankle joint trajectories.

Our research addresses a critical challenge in rehabilitation robotics: accurate prediction of lower-limb kinematics for personalized control of exoskeletons and prostheses without requiring extensive per-user calibration.



🌟 Key Features
Dual IMU Configuration: Uses two MPU6050 sensors (shank and foot) providing 12 raw features plus 4 complementary-filter-derived orientation features
Multi-horizon Prediction: Predicts both 20-step-ahead (200ms) and 50-step-ahead (500ms) ankle joint angles
Three Evaluation Paradigms:
Cross-subject (train on 5 subjects, test on 1)
Within-subject (80/20 split per subject)
Transfer learning (pretrain on 5 subjects, fine-tune on new subject)
Feature Augmentation: Incorporates complementary filter-derived roll/pitch angles to improve prediction accuracy
Complete Pipeline: From data acquisition to preprocessing, model training, and evaluation


📊 Results
Our approach achieved state-of-the-art results:

Cross-subject prediction: 3.57° MAE for 50-step-ahead (500ms) horizon
Within-subject prediction: 1.15° MAE for 50-step-ahead horizon
Transfer learning: 1.08° MAE for 50-step-ahead horizon (near within-subject performance with minimal user-specific data)
The transfer learning approach significantly reduces the calibration bottleneck in rehabilitation robotics, enabling rapid personalization with limited user-specific data.
