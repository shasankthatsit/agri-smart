🌱 AgriSmart – Plant Disease Detection & Crop Recommendation Web App


---

🏗 Project Overview

AgriSmart is a full-stack AI-powered web application designed for farmers and agriculture enthusiasts. It provides:

1. Plant Disease Predictor → Upload a crop leaf image, detect disease, and get preventive measures.


2. Crop Suggestor → Based on season (Kharif, Rabi, Zaid) and water requirements (Less, Moderate, More), it suggests suitable crops, fruits, and flowers.

Suggestions are displayed as flashcards with images, crop names, and growth time.



3. Educational Videos → Interactive category-based farming videos (Crops, Vermicompost, Advanced Farming), embedded within the app (no redirect, fullscreen option, only one plays at a time).



The website is responsive (works smoothly on laptops and mobiles) and has an animated UI with glassmorphism and zoom effects.


---

⚙️ Tech Stack

1. Frontend (Client-side)

HTML5 → Structure of the web pages (index, crop suggestor, disease predictor, videos).

CSS3 →

Responsive layouts for desktop and mobile.

Glassmorphism flashcards.

Stylish button-like navbar with hover effects.

Zoom-in animation for logo.


JavaScript (Vanilla JS) →

Dropdown-based filtering (videos, crop suggestor).

YouTube iframe control → ensures only one video plays at a time.

Responsive navbar toggling for smaller screens.




---

2. Backend (Server-side)

Python 3.x → Core backend language.

Flask (micro web framework) →

Handles routes (/, /predict, /crop_suggestor, /videos).

File upload handling for leaf image.

Renders templates with Jinja2.


Jinja2 Templating Engine →

Dynamic rendering: {{ prediction }}, {{ prevention }}, looping through suggestions to create flashcards.

Template inheritance via base.html.




---

3. Machine Learning / AI

TensorFlow / Keras → Pre-trained CNN model for plant disease classification.

NumPy, OpenCV, Pillow → Image preprocessing (resizing, normalizing, converting uploaded image).

Mapping dictionaries →

disease_classes → maps predicted class ID → disease name.

preventions → maps disease name → prevention methods.




---

4. Database

Currently, no database (static mappings in code).

Could extend with SQLite / PostgreSQL for storing user uploads, history, and feedback
