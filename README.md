# Teachable_Machine
Supervise Learning
# Image Classification Model

This repository contains a custom image recognition model trained using **Google Teachable Machine**. The model is designed to classify images in real-time via a web browser or integrated into JavaScript applications.

## 🔗 Live Model
You can test the model directly at the link below:
**[View Model on Teachable Machine](https://teachablemachine.withgoogle.com/models/BzRbMzug_Z/)**

---

## 🛠 Project Overview
This project uses **TensorFlow.js** to perform inference directly in the client's browser, meaning no data is sent to a server for processing.

### Classified Categories:
* **Class 1:** ["Backgroud"]
* **Class 2:** ["Empty Han"]
* **Class 3:** [Name of Class, e.g., "Wallet"]

## 🚀 Quick Start (Web Implementation)

To embed this model into your own web project, use the following boilerplate code:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a735ac3c-56d4-4ef2-b714-ec2efae2f56a" />


### 1. Include Dependencies
Add these scripts to your `index.html`:
```html
<script src="[https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@latest/dist/tf.min.js](https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@latest/dist/tf.min.js)"></script>
<script src="[https://cdn.jsdelivr.net/npm/@teachablemachine/image@latest/dist/teachablemachine-image.min.js](https://cdn.jsdelivr.net/npm/@teachablemachine/image@latest/dist/teachablemachine-image.min.js)"></script>
const URL = "[https://teachablemachine.withgoogle.com/models/BzRbMzug_Z/](https://teachablemachine.withgoogle.com/models/BzRbMzug_Z/)";

let model, webcam, labelContainer, maxPredictions;

async function init() {
    const modelURL = URL + "model.json";
    const metadataURL = URL + "metadata.json";

    // Load the model and metadata
    model = await tmImage.load(modelURL, metadataURL);
    maxPredictions = model.getTotalClasses();
    
    console.log("Model Loaded Successfully");
}
