# ucla_ajl_team_6 Skin Condition Classification

## Project Overview
This project focuses on detecting 21 different skin conditions across diverse skin tones using deep learning. The model leverages a pre-trained Xception network to classify skin conditions based on image data. The dataset consists of labeled skin images, and the model is trained to improve accuracy and generalization across various skin tones.

## Features
- **Image Preprocessing**:
  - Filters out corrupted images using JFIF metadata validation.
  - Analyzes image dimensions and channels for dataset exploration.
  
- **Data Augmentation**:
  - Implements rotation, width/height shifts, shear, zoom, horizontal flipping, and brightness adjustments to improve model robustness.
  
- **Model Architecture**:
  - Uses Xception as a base model (pre-trained on ImageNet) with additional fully connected layers.
  - Includes dropout for regularization and prevents overfitting.
  - Trains on categorical cross-entropy loss with the Adam optimizer.

- **Training and Evaluation**:
  - Utilizes image generators for training and validation.
  - Tracks performance using accuracy and loss visualization.
  
- **Predictions and Output**:
  - Generates predictions on test data and saves the results to a CSV file.
  - Maps predicted labels back to their original class names for easy interpretation.

## Installation and Setup
### Prerequisites
- Python 3.x
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- scikit-learn
- Pillow

### Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/your-repo/skin-condition-classifier.git
   cd skin-condition-classifier
   ```
2. Create and activate a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Ensure Jupyter Notebook is installed and add the virtual environment to Jupyter:
   ```sh
   pip install jupyter
   python -m ipykernel install --user --name=venv --display-name "Python (venv)"
   ```

## Running the Project
1. **Prepare the dataset**:
   - Ensure images are stored in the correct directory.
   - Run the preprocessing script to filter invalid images and analyze dataset properties.

2. **Train the model**:
   - Open the Jupyter Notebook and select the virtual environment kernel (`Python (venv)`).
   - Execute the training cells to train the Xception-based model on the dataset.

3. **Evaluate and visualize results**:
   - The notebook will generate accuracy/loss plots for performance evaluation.

4. **Make predictions on test data**:
   - Run the prediction cells in the notebook.
   - Outputs predictions in `predictions.csv`.

## Current Outcomes
- A trained deep learning model capable of classifying 21 different skin conditions across diverse skin tones.
- Achieved an F1 score of 0.17743.
- Pipeline for training, validating, and testing skin condition classification models.

## Contributors
- Vanessa Orozco, Oscar Khaing, Shaina Wang, Donald Ton, Zophia Laud, Safia Boutaleb

