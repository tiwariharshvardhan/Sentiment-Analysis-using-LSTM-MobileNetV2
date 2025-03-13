# Sentiment-Analysis-using-LSTM-MobileNetV2

## **Overview**
This project implements a **multi-modal sentiment analysis model** by integrating **LSTM for text sentiment analysis** and **MobileNetV2 for image-based sentiment classification**. The model processes **social media text and images** to determine sentiment (Positive, Negative, Neutral) and is designed for **business insights, brand perception analysis, and trend identification**.

## **Features**
- **Fusion Model** combining **LSTM for text** and **MobileNetV2 for image sentiment analysis**  
- **Text Sentiment Analysis** using **IMDB dataset** and word embeddings  
- **Image Sentiment Classification** by mapping CIFAR-100 labels to sentiment categories  
- **Preprocessing**: Tokenization, embedding, normalization, and augmentation  
- **Optimized Training** using **TensorFlow & Keras** with high accuracy  
- **Deployable API** using **Flask** for real-time sentiment predictions (Under development)

## **Dataset**
- **Text Data**: IMDB Sentiment Dataset (tokenized, embedded, and preprocessed)  
- **Image Data**: CIFAR-100 (mapped to sentiment categories, normalized, and resized)  

## **Model Architecture**
1. **Text Processing**: Tokenization, stop-word removal, embedding, LSTM layers  
2. **Image Processing**: Pretrained **MobileNetV2** for feature extraction  
3. **Fusion Network**: Concatenation of **text and image features**, followed by a dense layer for final sentiment prediction  

## **Installation & Setup**
### **1. Clone the Repository**
```bash
git clone https://github.com/your-username/sentiment-analysis-fusion.git
cd sentiment-analysis-fusion
```

### **2. Install Dependencies**
```bash
pip install tensorflow numpy pandas nltk flask scikit-learn
```

### **3. Run the Model Training**
```bash
python train_model.py
```

### **4. Start the API for Real-Time Predictions**
```bash
python app.py
```

## **Usage (Proposed Working Interface)**
Send a **POST request** to the API with text and image input:
```json
{
  "text": "The product is amazing!",
  "image": "path/to/image.jpg"
}
```

The API will return the **predicted sentiment**:
```json
{
  "sentiment": "Positive"
}
```

## **Future Improvements**
- Implement **BERT for advanced text processing**
- Enhance **emotion classification in images** using a larger dataset
- Deploy as a **cloud-based API** for real-time analysis

## **License**
This project is open-source under the **MIT License**.

