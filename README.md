# GoogleSolutions_2 – Image Metadata and Face Recognition Toolkit

This Jupyter Notebook combines facial recognition and image metadata analysis using DeepFace, Google Vision API, and various geolocation tools.

## Features

- Face detection and analysis with `DeepFace`
- Image label and text detection using `Google Cloud Vision API`
- EXIF metadata extraction
- GPS coordinate conversion and distance calculations with `haversine` and `geopy`
- Integration with Google Maps for reverse geocoding
- Firebase support (optional)

## Requirements

- Python 3.7+
- Jupyter or Google Colab environment
- Google Cloud credentials (Vision, Maps)
- (Optional) Firebase credentials

## Installation

Install required packages:

```bash
pip install -r requirements.txt
```
Running the Notebook
Open the notebook:

open it directly in Google Colab

Follow the cells top to bottom. The notebook:

Installs dependencies

Asks for image uploads

Processes image EXIF, faces, and GPS info

🔐 API Configuration Instructions
Google Cloud Vision API
Create a Google Cloud project: console.cloud.google.com

Enable the Vision API and Geocoding API

Create a service account key (JSON)

Upload the JSON key file and set the environment variable in your notebook:

python
Copy
Edit
import os
os.environ["GOOGLE_APPLICATION_CREDENTIALS"] = "your_key_file.json"
Google Maps
Create a key at Google Maps Platform, then:

python
Copy
Edit
gmaps = googlemaps.Client(key="YOUR_API_KEY")
Firebase (Optional)
Set up Firebase at firebase.google.com

Download firebase-adminsdk JSON file

Initialize in the notebook:

python
Copy
Edit
import firebase_admin
from firebase_admin import credentials, firestore

cred = credentials.Certificate("firebase_key.json")
firebase_admin.initialize_app(cred)
Author
Arush Badhe

---

## ✅ `requirements.txt`

```txt
deepface
google-cloud-vision
exifread
geopy
haversine
googlemaps
pandas
firebase-admin
Pillow
