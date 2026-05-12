#  Gender, Glasses, and Shirt Color Detection

This project detects **gender**, **glasses**, and **shirt color** from face images using a combination of pretrained and custom-trained models.

---

##  Requirements

Install the required libraries before running:

```bash
pip install deepface opencv-python pillow matplotlib torchvision
```

---

##  Dataset Preparation

1. Make sure your dataset is in a `.zip` file format (e.g., `images.zip`).
2. Each image should be in `.jpg` format and contain a visible face.
3. The script will prompt you to upload the zip file — it will extract images automatically.

---

##  How to Run the Solution

### Step 1: Open Google Colab

- Upload the provided Python file: `gender_glasses_shirtcolor_detection.py`

### Step 2: Upload Dataset

- When prompted, upload your zipped dataset of face images.
- The script will extract and detect all `.jpg` images in the folder.

### Step 3: Run the Script

- The script will:
  - Detect the face
  - Predict gender using **DeepFace**
  - Predict glasses using **ResNet-18**
  - Estimate shirt color from the image

### Example Output:

```
Image: face1.jpg
1- Gender: Female
2- Wearing Glasses: No
3- Shirt Color: RGB(123, 200, 150)
```

Each image will be visualized with predicted labels.

---

##  Notes

- Ensure images are clear and faces are visible.
- DeepFace may take 1–2 seconds per image.
- Glasses detection relies on a ResNet-18 model.
- Shirt color is estimated from the region below the detected face.

---

##  Model Info

- Gender: DeepFace (pretrained)
- Glasses: ResNet-18 (custom classifier)
- Shirt Color: Average RGB pixel values

---

##  File Structure

```
├── gender_glasses_shirtcolor_detection.py
├── images.zip  # Your input dataset
└── README.md
```
