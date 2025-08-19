# PHM

## （x / y / z 軸振動、電壓）4種訊號， 健康(Healthy)與 故障 (Faulty1 & Faulty2) 的疊加波形圖，
##  用於直觀觀察不同故障型態的振動幅值差異
![X-axis Vibration signals](X-axis_vib_signal.png)
![Y-axis Vibration signals](Y-axis_vib_signal.png)
![Z-axis Vibration signals](Z-axis_vib_signal.png)
![Voltage signals](vol_signal.png)

## 針對4種訊號，皆各進行20種的特徵提取(12個時域特徵:下圖 & 8個頻域特徵: 快速傅立葉一倍頻~八倍頻)，共有80個特徵
![Time-domain features (part 1)](時域特徵_1.png)
![Time-domain features (part 2)](時域特徵_2.png)

## 費雪法則(Fisher Score)的公式與示意圖介紹

Fisher Score 以「**類間均值差距** / **類內變異**」
來評分每一個特徵；差距越大且類內越集中者，分數越高、可分性越好。
![Fisher Score formula](Fisher_Score_公式.png)
![Fisher Score illustration](Fisher_Score_示意圖.png)

## 計算特徵之Fisher Score，以voltage-mean, voltage-Shape Factor的分數最高，以這些特徵來完成後續之分群之依據。
![Top-15 features by Fisher score](Fisher_Score_rank_result.png)

## 由以下架構方式，完成專案
![Project Core](Project_Core.png)

## 結果
![LR + PCA (Accuracy ≈ 100%)](LR_PCA_100.png)
![SVM + PCA (Accuracy ≈ 100%)](SVM_PCA_100.png)
![KNN + Fisher (Accuracy ≈ 97.22%)](KNN_FisherScore_97.png)
![LR + Fisher (Accuracy ≈ 97.22%)](LR_FisherScore_97.png)
![SVM + Fisher (Accuracy ≈ 94.44%)](SVM_FisherScore_94.png)






