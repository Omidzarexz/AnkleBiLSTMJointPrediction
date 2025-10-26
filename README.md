# Ankle Joint Trajectory Prediction During Gait from Dual IMU Sensors Using Bi-LSTM Networks and Transfer Learning



This repository contains the implementation code and dataset for our research on predicting ankle joint trajectories using dual IMU sensors and deep learning techniques. The work was presented in the ICROM 2025 conference paper titled "Ankle Joint Trajectory Prediction During Gait from Dual IMU Sensors Using Bi-LSTM Networks and Transfer Learning".

## 📌 Overview

This project proposes a bidirectional long short-term memory (Bi-LSTM) network to predict 20-step-ahead (200 milliseconds) and 50-step-ahead (500 milliseconds) ankle joint angles using IMU data from two wearable sensors (mounted on shank and foot). The system was validated against optical encoder ground truth measurements from six healthy subjects.

Key features of our approach:
- Uses two MPU6050 IMU sensors providing 12 raw features plus 4 complementary-filter-derived orientation features (16 total)
- Implements a stacked Bi-LSTM architecture for capturing temporal dependencies in gait data
- Features transfer learning capabilities to adapt to new users with minimal calibration data
- Achieves clinical-grade accuracy with minimal hardware requirements

## 📊 Key Results

Our framework demonstrates:
- **3.57° MAE** for 50-step-ahead prediction in cross-subject evaluation
- **1.15° MAE** for 50-step-ahead prediction in within-subject evaluation
- **1.08° MAE** for 50-step-ahead prediction using transfer learning (approaching within-subject performance with minimal user-specific data)
- **6.25× speed advantage** over real-time requirements, making it suitable for real-time applications

These results demonstrate that IMU sensors combined with Bi-LSTM networks can achieve accurate and generalizable prediction of ankle joint angles, providing a template for low-cost, portable gait analysis in clinical and community settings.

## 📚 Citation

If you find this work useful for your research, please cite our paper:

```
@inproceedings{zare2025ankle,
  title={Ankle Joint Trajectory Prediction During Gait from Dual IMU Sensors Using Bi-LSTM Networks and Transfer Learning},
  author={Zare Banadkouki, Omid and Zareinejad, Mohammad and Bahrami, Mohsen},
  booktitle={International Conference on Robotics and Mechatronics (ICROM)},
  year={2025}
}
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, fork the repository and send pull requests.

## 📧 Contact

For questions about the repository or the research:
- Omid Zare Banadkouki - [omid.zare@aut.ac.ir](mailto:omid.zare@aut.ac.ir)
- Mohammad Zareinejad - [mzare@aut.ac.ir](mailto:mzare@aut.ac.ir)
- Mohsen Bahrami - [mbahrami@aut.ac.ir](mailto:mbahrami@aut.ac.ir)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*This research was conducted at the Department of Mechanical Engineering, AmirKabir University of Technology, Tehran, Iran.*
