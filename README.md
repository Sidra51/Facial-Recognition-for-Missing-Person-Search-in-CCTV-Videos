# Facial-Recognition-for-Missing-Person-Search-in-CCTV-Videos


This project leverages deep learning and facial recognition to assist in locating missing persons using CCTV footage. By analyzing real-time or recorded video frames, the system matches detected faces against a reference database of missing individuals.

## 🔍 Objective

To automate the search for missing individuals in public surveillance videos using facial recognition technology, thereby reducing manual effort and increasing the chances of timely identification.

## 📌 Features

- Face detection and recognition using OpenCV and deep learning models
- Comparison of CCTV video faces with a database of missing persons
- Real-time or recorded video support
- Image preprocessing and face embedding generation
- Alert generation when a potential match is found

## 🛠️ Tech Stack

- Python
- OpenCV
- face_recognition (based on dlib)
- NumPy
- TensorFlow / Keras (if deep learning used)
- Streamlit (optional for UI)
- SQLite / CSV for storing known face encodings

## 🗂️ Project Structure

Facial-Recognition-for-Missing-Person-Search-in-CCTV-Videos/
│
├── dataset/ # Images of missing persons
├── CCTV_videos/ # Sample CCTV videos
├── encodings.pickle # Serialized known face encodings
├── recognize.py # Main script for face recognition from video
├── encode_faces.py # Script to generate encodings from dataset
├── utils/ # Helper functions (preprocessing, I/O, etc.)
├── requirements.txt # Required Python libraries
└── README.md # Project documentation

bash
Copy
Edit

##  How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Sidra51/Facial-Recognition-for-Missing-Person-Search-in-CCTV-Videos.git
cd Facial-Recognition-for-Missing-Person-Search-in-CCTV-Videos
2. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Prepare your dataset
Place clear frontal face images of missing persons in the dataset/ folder. Filenames should be the person's name or ID.

4. Generate encodings
bash
Copy
Edit
python encode_faces.py
5. Run the recognition script
bash
Copy
Edit
python recognize.py
You can modify the video input in the script (recognize.py) to use live feed or a saved video file.

Output
Names of matched persons displayed on-screen in real-time

Optional: Save frames of matched detections in a separate folder

Log file or terminal output showing match confidence

Limitations
Accuracy depends on video quality, lighting, and angle of face

Not effective with occluded or profile faces

Requires clear reference images for reliable matches

Future Enhancements
Integrate with public databases or police records

Support for low-resolution face enhancement

Add GUI using Streamlit or Flask

Email/SMS alert system
