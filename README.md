# Ingredient-Scanning-Application

The Ingredient Scanning Application is an AI-powered tool that detects and extracts ingredients from food product labels using object detection and OCR. It compares the extracted ingredients with a preloaded database, including FSSAI-approved food ingredient data, to determine whether the ingredients are healthy, harmful, or restricted. The system uses advanced text similarity techniques (TF-IDF + Cosine Similarity) to ensure accurate matching, even if the input is noisy or unclear.

# What the Project Is

Your Ingredient Scanning Application is an AI-powered tool that:

1. Detects ingredients or product labels from images using object detection (YOLO)
2. Extracts the text using OCR (pytesseract).
3. Matches it with a predefined list (maybe from an Excel or CSV using pandas).
4. Then compares text similarity using TF-IDF + Cosine Similarity to identify exact or related ingredients.
5. Finally, displays matched results with relevant nutritional or other information.

# Features of the Application

📷 Image Upload or Webcam Input to capture product labels.

🧠 YOLOv8 Model to detect the region of interest (like ingredient areas).

🔍 OCR with pytesseract to extract printed or handwritten text.

📊 Text Similarity Matching using TF-IDF and cosine similarity.

📁 Matches results against a nutritional dataset (like a CSV or Excel file).

🎯 Highly accurate ingredient recognition even with partial or blurry text/

# Required Installation & Libraries

1. Install OpenCV
   
Used for image and video processing.

`pip install opencv-python`

2. Install pytesseract (Python wrapper for Tesseract OCR)
   
`pip install pytesseract`

3. Install Tesseract-OCR Engine (Required for pytesseract)
   
For Windows:

1. Download from:
   
`👉 https://github.com/UB-Mannheim/tesseract/wiki`

2. Install it. Default path:

`C:\Program Files\Tesseract-OCR\tesseract.exe`

3. Add the following line in your Python code to link it:

`import pytesseract`

`pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'`

 For Linux:
 
`sudo apt update`

`sudo apt install tesseract-ocr`

For Mac:

`brew install tesseract`

4. Install YOLOv8 (via Ultralytics)

Used for object detection:

`pip install ultralytics`

You can test the installation with:

`yolo help`

5. Install Pillow

Used to handle image files (works with `Image` from PIL)

`pip install pillow`

6. Install Pandas

For reading/writing and handling Excel or CSV files.

`pip install pandas`

7. Install Scikit-learn

Used for text processing (TF-IDF, cosine similarity).

`pip install scikit-learn`

# How It Works (Step-by-Step)

1. Capture or upload an image with product ingredients.
2. The YOLOv8 model identifies regions with text (optional: filter out unnecessary objects).
3. Pytesseract OCR extracts ingredient text from detected areas.
4. The extracted text is processed using TF-IDF Vectorization.
5. It is compared against a predefined ingredient database using cosine similarity.
6. Matched results (e.g., sugar, salt, preservatives) are shown to the user.
7. The app can show nutritional or allergy-related data using `pandas`.

# Example Output

Input image: Front of a packaged food item

Extracted text: "sugar, maltodextrin, palm oil"

Output:

Ingredient: Sugar — High in calories, avoid excess

Ingredient: Palm Oil — Contains saturated fats

Ingredient: Maltodextrin — High glycemic index

# Difference from Other Applications

| Feature                                   | Our App   | Other Apps                |
| ----------------------------------------- | --------   | ------------------------ |
| Uses YOLO for object detection            | ✅ Yes    | ❌ Mostly direct OCR only |
| TF-IDF + Cosine Similarity for accuracy   | ✅ Yes    | ❌ Rare                   |
| Works offline                             | ✅ Yes    | ❌ Needs cloud            |
| Integrated data comparison with Excel/CSV | ✅ Yes    | ❌ Not always available   |
| Customizable ingredient list              | ✅ Yes    | ❌ Hardcoded or limited   |

#  Future Scope

1. Build a mobile app (Android/iOS) for real-time ingredient scanning.
2. Add a voice-based description for each ingredient (via TTS).
3. Add allergy detection alerts based on user profiles.
4. Connect with a larger product database API for barcode scanning.
5. Nutrition scoring & recommendations (e.g., "Healthier alternatives").

# Contributions

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

# Contact

Project Owner: Priyanshi Chaudhary

Email: priyanshichaudhary2015@gmail.com

