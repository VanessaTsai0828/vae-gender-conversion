# VAE-Based Gender Transformation on Face Images  
🧠 使用 VAE 實現臉部性別轉換：將男性臉孔轉換為個人化的女性版本，保留原始特徵與風格。含 latent 空間分析與完整視覺化展示。
🧬 Gender transformation using Variational Autoencoder: Converts male faces into personalized female versions via latent vector editing. Includes t-SNE visualization and identity preservation.

## 📌 Project Description 專案介紹

This project explores the use of a Variational Autoencoder (VAE) to modify facial features along a learned "gender direction" in latent space.  
本專案透過變分自編碼器（VAE），在潛在空間中尋找「性別方向向量」，將人臉進行個人化的性別轉換（例如從男性轉為對應的女性臉）。

The goal is to preserve the identity while applying semantic transformations (e.g., feminine version of each face).  
目標是保留原人物特徵的前提下，生成該人的女性版本臉孔，實現語意上的轉換能力。

---

## 🧠 Model Architecture 模型架構

- **Encoder**: Convolutional layers to compress images into latent vectors  
  編碼器：將圖片壓縮成潛在向量（Latent Vector）
- **Decoder**: Transposed convolutions to reconstruct images from latent space  
  解碼器：從潛在空間中還原圖片
- **Latent Vector Arithmetic**: Gender direction vector = (female mean) - (male mean)  
  性別向量操作：計算潛在空間中 female - male 的平均差值，用來做轉換

---

## 🎯 Features 核心特色

- Supports gender vector interpolation for **personalized female face generation**  
  支援使用性別向量做潛在空間插值，產生個人化女性臉孔
- t-SNE visualization to observe **latent space distribution**  
  提供 t-SNE 降維圖觀察訓練與驗證資料在潛空間中的分布情形
- Before/After image comparison with **custom plotting**  
  可視化前後對照結果（原始臉 → 女版臉），呈現模型效果

---

## 🖼️ Sample Results 範例輸出
![image](https://github.com/user-attachments/assets/10b651f0-bc28-43dd-a3b9-4a11d0595cd7)


---

## 📊 t-SNE Visualization 潛在空間視覺化
![image](https://github.com/user-attachments/assets/48a0d851-1fc1-4438-ba8d-973d1207e74b)


---

## 📉 Training Loss Curve 訓練曲線
![image](https://github.com/user-attachments/assets/5df64d04-2a65-499b-ac9e-5c584702d204)


