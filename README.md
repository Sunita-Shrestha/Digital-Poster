```markdown
# Teachable Machine Model Documentation

## 📌 Model Link

🔗 https://teachablemachine.withgoogle.com/models/aiHUQmOcm/

> This is a machine learning model trained using Google’s *Teachable Machine*, an easy web tool for creating image, sound, or pose models without coding. :contentReference[oaicite:1]{index=1}

---

## 🧠 Overview

This model was created with **Teachable Machine**, a browser-based tool by Google that lets you train neural network classifiers using your own examples. You can train the model on:
- Images
- Audio
- Pose data

It uses *TensorFlow.js* under the hood, and the output can be exported for use in websites, apps, or other software. :contentReference[oaicite:2]{index=2}

---

## 📂 Exported Model Files

When you export a Teachable Machine model, you usually get:

```

/model.json           # Model architecture and weights
/metadata.json        # Class names and labels
/weights.bin          # Binary weight data

````

---

## 🤖 How It Works

1. **Collect Data**  
   You provide sample images, sounds, or poses for each class you want the model to recognize. :contentReference[oaicite:3]{index=3}

2. **Train the Model**  
   Teachable Machine trains a neural network live in your browser. :contentReference[oaicite:4]{index=4}

3. **Export the Model**  
   After training, you can download or host the model files to use in code. :contentReference[oaicite:5]{index=5}

4. **Use in Projects**  
   The model can be run in JavaScript apps (e.g., web pages) using TensorFlow.js, or converted into formats like TensorFlow Lite for mobile. :contentReference[oaicite:6]{index=6}

---

## 🧪 Example: JavaScript Integration

Here’s a simple example of loading the model in a web page using the TensorFlow.js library:

```html
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@latest"></script>
<script src="https://cdn.jsdelivr.net/npm/@teachablemachine/image@latest"></script>

<script>
const URL = "https://teachablemachine.withgoogle.com/models/aiHUQmOcm/";

async function init() {
  const modelURL = URL + "model.json";
  const metadataURL = URL + "metadata.json";

  const model = await tmImage.load(modelURL, metadataURL);
  console.log("Model loaded!");

  // Example: classify an image element
  const imageElement = document.getElementById("inputImage");
  const prediction = await model.predict(imageElement);
  console.log(prediction);
}

init();
</script>
````

> This code uses the Teachable Machine Image library to load and predict with the model. ([DeepWiki][2])

---

## 🛠️ How to Use the Model

To use your model:

1. **Train and export it** from Teachable Machine. ([experiments.withgoogle.com][1])
2. **Host the files** somewhere public (GitHub, cloud storage, etc.).
3. **Load the model in code** (JavaScript, mobile app, Python script, etc.).
4. **Feed input** (images, audio, or pose data) to the model to classify.

---
---
# My Model
## Image Classification Model – Teachable Machine

## 📌 Model Overview

This is an image classification model created using Google Teachable Machine.

The model is trained to classify images into four categories:

1. Background  
2. Sunita  
3. Phone  
4. Cup  

The model was trained using  image samples for each class.

---

## 🧠 Model Type

- Project Type: Image Project
- Platform: Teachable Machine
- Framework: TensorFlow.js
- Number of Classes: 4

---

## 📂 Classes Description

### 1️⃣ Background
Images that do not contain the main target objects.

### 2️⃣ Sunita
Images containing Sunita.

### 3️⃣ Phone
Images containing a mobile phone.

### 4️⃣ Cup
Images containing a cup.

---

## ⚙️ Training Process

1. Collected multiple image samples for each class.
2. Uploaded images into Teachable Machine.
3. Trained the model in the browser.
4. Evaluated predictions.
5. Exported the model for use in web applications.

---

## 📊 Model Output

The model predicts probabilities for each class.

Example output:

<img width="458" height="810" alt="phone" src="https://github.com/user-attachments/assets/f81762ef-471a-4a4e-bf00-1e9f2d750c7f" />
<img width="458" height="810" alt="cup" src="https://github.com/user-attachments/assets/6a924715-81a7-4f7c-9f1f-9658f531377e" />



## 📝 Notes

* The model page may not load on all devices; you might need desktop Chrome or Safari. ([teachablemachine.withgoogle.com][3])
* The actual model type (image/audio/pose) depends on how you trained it.

---

## 📚 References

* Teachable Machine is a no-code tool for training AI models in the browser. ([experiments.withgoogle.com][1])
* Exported models can be used in applications with TensorFlow.js or converted for mobile use. ([DeepWiki][4])

```

---

[1]: https://experiments.withgoogle.com/teachable-machine?utm_source=chatgpt.com "Teachable Machine by Google Creative Lab - Experiments with Google"
[2]: https://deepwiki.com/googlecreativelab/teachablemachine-community/4-javascript-integration?utm_source=chatgpt.com "JavaScript Integration | googlecreativelab/teachablemachine-community | DeepWiki"
[3]: https://teachablemachine.withgoogle.com/models/aiHUQmOcm/ "Teachable Machine"
[4]: https://deepwiki.com/googlecreativelab/teachablemachine-community/1-overview?utm_source=chatgpt.com "googlecreativelab/teachablemachine-community | DeepWiki"
