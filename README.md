
<h1>🚖 Smart Fare Prediction: Enhancing Taxi Pricing with Data-Driven Intelligence</h1>

<h2>Description</h2>
This project performs a comparative analysis of Graph Attention Networks (GAT), XGBoost, and TimesNet to predict NYC taxi fares under noisy and clean data conditions. Handled 55 million dataset. Using deep learning, tree-based models, and sequence models, we analyze how different architectures handle real-world complexities like noise, uncertainty, and temporal-spatial features.

<h3>Project Objectives</h3>
- Predict taxi fares using clean, noisy, and denoised data.

- Compare model robustness, generalization, and uncertainty estimates.

- Evaluate performance using metrics: MAE, MSE, R², calibration, OOD tests.

- Provide practical insights for model selection in transportation systems.

<h4>🧠 Models Implemented</h4>

| Model               | Type                   | Use Case             |
| ------------------- | -----------------------| -------------------- |
| <b>XGBoost</b>      | Ensemble Tree          | Tabular baseline     |
| <b>GAT</b>          | Graph Neural Network   | Spatial modeling     |
| <b>TimesNet</b>     | Temporal Deep Learning | Sequence forecasting |



<h5>🛠️ Features & Pipeline </h5>

- PySpark for scalable preprocessing.

- KNN Imputation for handling missing values.

- Gaussian Noise Injection and Autoencoder Denoising.

- Graph Construction: Trips are treated as nodes connected via fare similarity.

- Custom Metrics: ±10% accuracy, calibration plots, OOD performance evaluation.

<h6> 🧪 Performance Summary </h6>

| Model    | Dataset | MAE    | MSE    | R²     |
| -------- | ------- | ------ | ------ | ------ |
| XGBoost  | Clean   | 0.1040 | 0.0279 | 0.9910 |
| XGBoost  | Noisy   | 0.8203 | 1.4407 | 0.7326 |
| GAT      | Clean   | 1.1057 | 2.4414 | 0.2153 |
| GAT      | Noisy   | 2.5036 | 11.437 | -1.123 |
| TimesNet | Clean   | 1.3519 | 3.3534 | -0.077 |
| TimesNet | Noisy   | 1.7303 | 5.8836 | -0.091 |

XGBoost is most robust under noise; GAT captures spatial patterns but is sensitive to noise; TimesNet excels in temporal learning but struggles with generalization.

<h7> 🖥️ Google Colab Setup </h7>

Ensure google-colab is available.

Mount Google Drive: 
from google.colab import drive
drive.mount('/content/drive')

<h8> 📊 Evaluation Metrics </h8>

MAE: Mean Absolute Error

MSE: Mean Squared Error

R²: Coefficient of Determination

Calibration Plot: Predicted vs Actual

Uncertainty Estimation: Prediction intervals

OOD Testing: Generalization on noisy unseen data

<h8> 📁 Dataset Links </h8>

https://drive.google.com/file/d/1SdWurixKsWcQ-_F_IHQZhJWRzUk1odUh/view?usp=drive_link - INITIAL TRAIN DATA 
https://drive.google.com/file/d/1cfV4udBKpWj3vRNbI3Lyv9VjIsmb2zDR/view?usp=drive_link - NOISY TRAIN
https://drive.google.com/file/d/1-0HTq6LPQD6BH-ouOu-TvU0d8NLN81ni/view?usp=drive_link - NULL REMOVE 
https://drive.google.com/file/d/1-63Prav-4wodgE7WjhFKHM3Js-_9cSIh/view?usp=drive_link - AFTER HAVERSINE DISTANCE
https://drive.google.com/file/d/1-QJGzMniVtY_D977FoKPwcKeAt3njnaq/view?usp=drive_link - TRAIN DATA AFTER PREPROCESSING
https://drive.google.com/file/d/1-16lrlkTiAGq19dMhftfgUHve7eigtyN/view?usp=drive_link - OUTLIER REMOVED NOISY DATA
https://drive.google.com/file/d/1-J8b4l6iYfiVB3uEqdAvsZ9UqrK07jXN/view?usp=drive_link - AUTO ENCODER DENOISING
https://drive.google.com/file/d/1Wub3Rtszs7JohBtogS679k2p2Gh8-zFN/view?usp=drive_link - GRAPH FOR GNN DENOISED
https://drive.google.com/file/d/1yTz3b1Y192jSLGR-GDuTVfyypaHwWBgh/view?usp=drive_link - GRAPH FOR GNN NOISY
https://drive.google.com/file/d/1AeA3501RYAMuf9AckMnBy-_W3bYCG5xS/view?usp=drive_link - GAT DENOISED 
https://drive.google.com/file/d/1m8nbQExz10e122mwz5flb22odBfpG14P/view?usp=drive_link - GAT NOISE
https://drive.google.com/file/d/11TTdPeTa5UE60nRJEcc8JWvXeGOYP4zb/view?usp=drive_link - XGBOOST DENOISED
https://drive.google.com/file/d/1yUriLBpPgE_jzA54FIo82u7gVWbt03L0/view?usp=drive_link - XGBOOST NOISY
https://drive.google.com/file/d/165mA-6XlyWemjUgwEPDZF07IqS3Lpzxa/view?usp=drive_link - TIMESNET DENOISED
https://drive.google.com/file/d/1oAFz749wrnjgbS1OnNxJRnmLzjakfs1V/view?usp=drive_link - TIMESNET NOISE
