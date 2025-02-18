# NeuroFusion
![1](https://github.com/user-attachments/assets/c2cfd4e9-6d6d-4eeb-bee0-e84d0b9b8ad8)


# EEG Signal Summarization with Deep Learning  

## 🧠 Project Overview  
This project focuses on processing EEG signals for summarization and classification using deep learning. The model is built using **TorchEEG** and incorporates the **ArjunViT** architecture for feature extraction and classification. The pipeline includes preprocessing EEG data, training a neural network, and exporting the model to **ONNX** format for optimized deployment.  

## 🚀 Features  
- EEG signal preprocessing and normalization  
- **ArjunViT** for EEG feature extraction  
- Training and evaluation with **PyTorch**  
- ONNX model export for efficient inference  
- Supports the **DREAMER** dataset (customizable for other EEG datasets)  

## 📦 Installation  
1. Clone the repository:  
   ```sh
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```  
2. Create a virtual environment and install dependencies:  
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   pip install -r requirements.txt
   ```  

## 📊 Dataset  
This project uses the **DREAMER** dataset for EEG-based emotion recognition. You can download the dataset from [official sources](https://zenodo.org/records/546113). The dataset needs to be preprocessed before training.  

## 🔧 Usage  
### 1️⃣ Preprocess the Data  
Run the preprocessing script to normalize and transform EEG signals:  
```sh
python preprocess.py
```  

### 2️⃣ Train the Model  
Train the **ArjunViT** model on the EEG dataset:  
```sh
python train.py
```  

### 3️⃣ Export Model to ONNX  
Convert the trained model to **ONNX** format for optimized deployment:  
```sh
python export_onnx.py
```  

### 4️⃣ Inference  
Run inference using the trained model on test data:  
```sh
python inference.py --model model.onnx --input sample_eeg.npy
```  

## 📌 ONNX Model Export  
The model is exported to ONNX for efficient inference:  
```python
torch.onnx.export(model, dummy_input, "model.onnx", export_params=True, opset_version=11)
```   

## 🤝 Contributing  
Contributions are welcome! If you’d like to improve this project, follow these steps:  
1. Fork the repository  
2. Create a new branch (`git checkout -b feature-name`)  
3. Commit your changes (`git commit -m "Add feature"`)  
4. Push to the branch (`git push origin feature-name`)  
5. Open a Pull Request  

