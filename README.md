# SignTalk AI: Real-Time Sign Language to Audio Translator

SignTalk AI is a professional Machine Learning ecosystem developed using Python. It allows users to collect, train, and deploy custom sign language recognition models. The project is structured as a complete development pipeline, enabling the transformation of hand gestures into audible speech through a systematic four-step process.

---

## Development Workflow

The project is designed to be modular. To build the system or add new vocabulary to the dictionary, users must follow these steps in the specific order listed below:

### 1. Data Collection (src/01_Data_Collection.py)
The initial stage involves building a custom dataset of hand landmarks.
- Process: The script utilizes the camera and MediaPipe to track 21 specific hand landmark coordinates.
- Output: The x, y, and z coordinates are captured in real-time and stored in a file named sign_data.csv.
- Purpose: To establish a foundation of raw data for every gesture intended for recognition.

### 2. AI Model Training (src/02_Training_Model.py)
After collecting the data, the AI must be trained to recognize the patterns within the coordinates.
- Process: This script processes the sign_data.csv file using Machine Learning algorithms to classify the gestures.
- Output: The system generates an Accuracy Percentage, providing a metric of the model's reliability.
- Purpose: To create the intelligence layer required for real-time predictions.

### 3. Visual Prototype Testing (src/03_Final_Translator.py)
This stage serves as an intermediate testing phase to verify the model's performance visually.
- Interface: The output is displayed as text on the camera feed within a basic user interface.
- Features: This version does not include audio output. It is focused solely on the accuracy and stability of gesture detection.
- Purpose: To ensure the model predicts gestures correctly before moving to full application deployment.

### 4. Final Application and Deployment (src/04_APP.py)
This is the final stage that results in a complete, ready-to-use Windows application.
- Interface: Features a refined and professional user interface.
- Main Features: Integrates real-time gesture detection with both text display and automated audio output via Google Text-to-Speech (gTTS).
- Purpose: To provide a functional communication tool that bridges the gap between sign language and spoken language.

---

## Adding New Vocabulary
SignTalk AI is built to be dynamic. If a user wishes to add new words or inputs, they must follow this cycle:
1. Run Step 1 (01_Data_Collection.py) to record the new gesture data.
2. Re-run Step 2 (02_Training_Model.py) to update the AI model with the new information.
3. Run Step 3 or Step 4 to utilize the updated system.

---

## Tech Stack and Requirements
The following libraries are required to run this project:

| Library | Function |
| :--- | :--- |
| OpenCV | Video and camera frame processing |
| MediaPipe | Hand landmark coordinate extraction |
| Scikit-Learn | Machine Learning algorithms and classification |
| Pandas and NumPy | Data manipulation and array processing |
| gTTS | Text-to-speech synthesis |
| Pygame | Low-latency audio playback |

### Installation:
```bash
# Clone the repository
git clone [https://github.com/username/SignTalk-AI.git](https://github.com/username/SignTalk-AI.git)

# Navigate to the project directory
cd SignTalk-AI

# Install dependencies
pip install -r requirements.txt
