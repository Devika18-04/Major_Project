# Project Title : Pneumonia Detection Using CNN: A Deep Learning Approach
This project aims to develop a Deep Learning model which analyses chest X-ray images and identify penumonia. The model classifies images into two categories: 'Pneumonia' and 'Normal'.​
## Features
- Automated Pneumonia Detection
- Binary Classification
- Scalable & Reusable
- Portable Model Saving
- User-friendly interface
## Tech Stack
- Backend: Python, Flask
- Frontend: Html, CSS, Javascript
- Models: EfficientNet-B0, VGG16
## Prerequisites
- Python 3.11 or higher
- Flask
- Anaconda
- Jupyter notebook
## Dataset
The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal). Chest X-ray 
mages (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five 
ears old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was perf
-ormed as part of patients’ routine clinical care. For the analysis of chest x-ray images, all chest radi-
iographs were initially screened for quality control by removing all low quality or unreadable scans. The
diagnoses for the images were then graded by two expert physicians before being cleared for training the 
AI system. In order to account for any grading errors, the evaluation set was also checked by a third expert.
Click here to download dataset [here](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)

  

## Step by step procedure for model development 
1. **Problem Definition**
   - **Identify the goal**: detect pneumonia from chest X-ray images using deep learning.
2. **Data Collection**
   - Download and organize the labeled chest X-ray dataset (Normal vs Pneumonia) from kaggle.
3. **Data Preprocessing**
    - Resize images to a standard size
    - Normalize pixel values
    - Apply augmentation for better generalization
4. **Model Building**
    - Use transfer learning with a pretrained model like VGG16 and EfficientNet-B0 load from ImageNet
5. **Model Compilation**
    - Set loss function (binary_crossentropy)
    - Use Adam optimizer and monitor accuracy
6. **Model Training**
    - Fit the model on training data and validate on a holdout set. Monitor loss and accuracy over epochs.
7. **Model Evaluation**
    - Evaluate performance on test data. Plot confusion matrix, accuracy, precision, and recall.
8. **Model Saving**
    - Save the best model based on accuracy using model.save('best_model.h5')
9. **Deployment**
    - Build a simple Flask app to upload and predict X-rays via web interface.

## Usage
1. **Run the Flask Application**
   ```bash
   flask run
   ```
2. **Access the webpage**
   Open the browser and go to `http://127.0.0.1:5000` to use the web application
## Project Structure
```
Pneumonia_Detection/
├── chest_xray/
│   │  ├──test/
│   │  │  ├──NORMAL/
│   │  │  └──PENUMONIA/
│   │  ├──train/
│   │  │  ├──NORMAL/
│   │  │  └──PNEUMONIA/
│   │  ├──val/
│   │  │  ├──NORMAL/
│   │  │  └──PNEUMONIA/
├── Images/
│   │  ├──category_distribution_bar.png 
│   │  ├──category_distribution_pie.png
│   │  ├──confusion_matrix.png
│   │  └──image_display.png
├── saved_models/
│   │  ├──best_model.h5  
├── static/
│   │   ├── css/
│   │   ├──js/
│   │   ├──img.jpeg
│   │   └──main.jpeg
├── templates/
│   │   ├──result.html
│   │   └── index.html
├── uploads/   
├── app.py
├── classification_report.txt
├── Dataset_Visualization.ipynb
├── models_results.txt
├── pneumonia_detection_transfer_learning.ipynb
└── README.md
```
## Key files
- **`Pneumonia_Detection/templates/index.html`**: The main HTML file the application interface
- **`Pneumonia_Detection/app.py`**:The app.py file typically contains the main Flask application logic, including route definitions, model loading, and image prediction handling for the pneumonia detection system.
- **`Pneumonia_Detection/pneumonia_detection_transfer_leraning.ipynb`**: The file `pneumonia_detection_transfer_learning (2).ipynb` contains a transfer learning-based implementation using a pretrained model (likely VGG16 and EfficientNet-B0) to classify chest X-ray images into Pneumonia and Normal categories, enhancing performance with reduced training time.
## Project Ouput Images
1. Home page of the application [here](https://drive.google.com/file/d/1d9znJ6vk63_HBbLtDFe2XrOK8lHLHJNn/view?usp=drive_link)
2. Pneumonia chest x-ray image uploaded [here](https://drive.google.com/file/d/1RKhDq7klpBsSw-S7kbKn7lrr3iLF6VdJ/view?usp=drive_link)
3. Image classified as Pneumonia [here](https://drive.google.com/file/d/1O6Q3gRiKHu0WyFCtso253gpseN38pWjL/view?usp=drive_link)
4. Normal chest x-ray image uploaded [here](https://drive.google.com/file/d/1Bz0vsnS2mlNT7hIEgIjywYf9D5zwNtrX/view?usp=drive_link)
5. Image classified as Normal [here](https://drive.google.com/file/d/1chQDDWYuB22FavN1DZGZ5Bz0oxhwhTSs/view?usp=drive_link)
## Project Execution Video
For a detailed demonstration of Pneumonia Detection, you can watch the project video here [here](https://drive.google.com/file/d/1gTRoixlaL1WpGmOQ0CuSCidXgXaTJmxj/view?usp=drive_link)
   
