🚗 Car Colour Detection & People Counter
A machine learning project that detects cars in traffic images, identifies their colour, and counts people at traffic signals — using YOLOv8 and OpenCV.

🎯 What This Project Does
DetectionBox Colour🔵 Blue Car🔴 RED rectangle🚗 Other Colour Car🔵 BLUE rectangle🧍 Person🟢 GREEN rectangle

Counts total vehicles detected
Counts blue vehicles specifically
Counts people present at the signal
Displays summary on the image itself


🛠️ Tech Stack

YOLOv8 — Object detection (cars, people)
OpenCV — Image processing & colour detection
Python — Core language
Google Colab — Free cloud environment to run
Kaggle — Dataset source


🚀 How to Run (Step by Step)
Step 1 — Open in Google Colab

Go to https://colab.research.google.com
Click File → Upload Notebook
Upload the file car_color_detection.ipynb

Step 2 — Get Kaggle API Key

Go to https://www.kaggle.com
Click your Profile picture → Settings
Scroll to API section → Click Create New Token
A file called kaggle.json will download to your computer

Step 3 — Run the Notebook
Run each cell in order from top to bottom:

Cell 1 — Installs required libraries
Cell 2 — Upload your kaggle.json file when prompted
Cell 3 — Downloads the traffic dataset automatically
Cell 4 — Loads the YOLOv8 model
Cell 5 — Sets up detection functions
Cell 6 — Opens a GUI where you can upload your own image
Cell 7 — Tests on dataset images automatically


📂 Project Structure
car-color-detection/
│
├── car_color_detection.ipynb   ← Main notebook (run this)
└── README.md                   ← This file

📊 How Colour Detection Works

YOLOv8 detects each car and gives its bounding box coordinates
We crop that car region from the image
We convert the cropped region to HSV colour space (better for colour detection)
We check if more than 15% of pixels fall in the blue HSV range (Hue: 100–140)
If yes → RED rectangle. If no → BLUE rectangle


🖥️ Sample Output
══════════════════════════════════════
   🚗 CAR COLOUR DETECTION SYSTEM
══════════════════════════════════════
📊 Results:
   🚗 Total vehicles detected : 6
   🔵 Blue vehicles           : 1
   👤 People detected         : 3
══════════════════════════════════════

📦 Dataset Used
Traffic Vehicles Object Detection from Kaggle
kaggle datasets download -d saumyapatel/traffic-vehicles-object-detection
You can replace this with any traffic/car dataset from Kaggle.

🔧 Requirements
All installed automatically in the notebook:
ultralytics
opencv-python-headless
ipywidgets
Pillow
kaggle

👤 Author
Dhanushkumar Kuppusamy — Final Year BCA Student
Interested in Data Science & Machine Learning

📄 License
MIT License — Free to use and modify
