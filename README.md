# SpeakMySign ASL  ASL to Speech Converter
# overview
Speak My Sign is a real-time American Sign Language (ASL) to speech conversion system that uses computer vision and machine learning 
to interpret hand gestures and convert them into spoken words. This project captures ASL letter signs, trains a classification model,
and provides an interactive interface for sign-to-speech conversion.
# Key Features
1. Real-time ASL Recognition: Uses MediaPipe for hand tracking and landmark detection
2. Machine Learning Model: Random Forest classifier trained on custom-collected ASL dataset.
3. Interactive Interface:
Press keys A-Z to collect training data for each letter
Spacebar to confirm predictions
Enter to speak the recognized letters.
4. Text-to-Speech: Integrated pyttsx3 for voice output of recognized signs
# Technical Details
Data Collection: Captures 100 samples per ASL letter (A-Z, excluding J)
Model Performance:
90% overall accuracy, 
0.89-0.90 precision/recall across letters
See full classification report in notebook
# Installation
Clone this repository
Install required packages:
~pip install opencv-python mediapipe pyttsx3 pandas joblib scikit-learn
# Usage
Data Collection:
Run the first notebook cell to capture ASL samples
Press letter keys (A-Z) to start collecting samples for that letter
ESC to exit collection mode
Model Training:
The second cell trains and saves the Random Forest model
Sign Recognition:
The third cell loads the model for real-time prediction
Show ASL signs to camera
Press SPACE to confirm letter, ENTER to speak
# File Structure
signtospeeches.ipynb: Main Jupyter notebook with all code
new_asl_dataset.csv: Collected ASL landmark data
new_asl_model.pkl: Trained Random Forest model
# Performance Metrics
   Metric	Precision	Recall	F1-Score	Support
1. Accuracy	–	–	0.90	2999
2. Macro Avg	0.89	0.90	0.89	2999
3. Weighted Avg	0.90	0.90	0.90	2999
# Future Improvements
Add support for dynamic signs and full words
Improve model robustness with more diverse training data
Add user interface for easier interaction
Support for numbers and common phrases
# Dependencies
.Python 3.x
.OpenCV
.MediaPipe
.scikit-learn
.pandas
.joblib
.pyttsx3
# License
MIT License - Free for educational and personal use


