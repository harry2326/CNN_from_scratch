##  Explanation Video

 [Watch Full Explanation](https://drive.google.com/drive/folders/1_-jtJwKOcv7CjdoW2pPtc8PFlmIwcqbU?usp=sharing)

---

##  Overview

This project implements a **Convolutional Neural Network (CNN)** to classify traffic signs using the **German Traffic Sign Recognition Benchmark (GTSRB)** dataset.

The model learns to identify **43 different traffic sign classes** from colored images of size **32×32×3**.

---

##  Key Concepts Covered

* Image preprocessing & normalization
* One-hot encoding
* Convolutional Neural Networks (CNNs)
* Max pooling
* Fully connected layers
* Softmax classification
* Model training & evaluation
* Real-time prediction on test samples

---

##  Dataset

* Dataset: **Traffic Signs (GTSRB)**
* Classes: **43**
* Image size: **32 × 32 × 3**
* Files used:

  * `train.p`
  * `valid.p`
  * `test.p`
  * `signnames.csv`

---

##  Pipeline Breakdown

### 1. Data Loading

* Data is loaded from `.p` (pickle) files
* Extract:

  * `features` → images
  * `labels` → class IDs

---

### 2. Preprocessing

####  Normalization

[
\text{Pixel values: } 0 \rightarrow 255 \Rightarrow 0 \rightarrow 1
]

####  One-Hot Encoding

* Converts labels into vectors of size 43
* Required for multi-class classification

---

##  Model Architecture

###  Convolutional Layers

1️⃣ Conv Layer

* Filters: 6
* Kernel: 5×5
* Output: 28×28×6

2️⃣ Max Pooling

* Output: 14×14×6

3️⃣ Conv Layer

* Filters: 16
* Kernel: 5×5
* Output: 10×10×16

4️⃣ Max Pooling

* Output: 5×5×16

---

### 🔹 Fully Connected Layers

* Flatten
* Dense (120 neurons, ReLU)
* Dense (80 neurons, ReLU)
* Output Layer (43 neurons, Softmax)

---

##  Loss Function

[
\text{Categorical Crossentropy}
]

---

##  Optimizer

* **Adam Optimizer**

---

##  Training

* Batch size: **128**
* Epochs: **3**
* Validation data used during training

---

##  Evaluation

* Model evaluated on test dataset
* Outputs:

  * Test accuracy
  * Loss

---

##  Prediction

* Random test image is selected
* Model predicts class probabilities
* Displays:

  * Predicted label & name
  * True label & name

---

##  Requirements

Install dependencies:

```bash id="p7z4jd"
pip install tensorflow numpy pandas matplotlib
```

---

##  Usage

1. Set dataset path:

```python id="q2a9df"
os.chdir('path_to_dataset_folder')
```

2. Run the script:

```bash id="z8k3pl"
python traffic_sign_classifier.py
```

3. Output:

* Training logs (loss & accuracy)
* Final test accuracy
* Random prediction result

---

##  Project Structure

```id="v9m2lx"
.
├── traffic_sign_classifier.py
├── train.p
├── valid.p
├── test.p
├── signnames.csv
└── README.md
```

---

##  Features

✔ CNN built using Keras Sequential API
✔ Multi-class classification (43 classes)
✔ Real-time prediction demo
✔ Clean modular pipeline

---

##  Limitations

* Low number of epochs (only 3)
* No data augmentation
* No dropout (risk of overfitting)
* Basic architecture (can be improved)

---

##  Future Improvements

* Increase epochs for better accuracy
* Add Dropout layers
* Use Batch Normalization
* Data augmentation (rotation, brightness, etc.)
* Try deeper architectures (ResNet, VGG)
* Convert to real-time camera-based detection

---

##  Contributing

Feel free to fork and improve the project!

---

##  License

You can add an MIT License to make this project open-source.

---

