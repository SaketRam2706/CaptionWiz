# CaptionWiz

## Overview

**CaptionWiz** is a web application that generates descriptive captions for images using a deep learning model combining Convolutional Neural Networks (CNN) and Transformer architectures. The app is built with Flask and leverages TensorFlow for model inference. Users can upload an image through the web interface and receive an AI-generated caption.

---

## Features
- Upload an image and receive an automatic caption.
- Uses a custom-trained model with InceptionV3 and Transformer layers.
- Simple web interface (Flask-based).
- Supports image augmentation and advanced captioning techniques.

---

## Directory Structure

```
CaptionWiz/
│
├── app.py                # Main Flask application
├── README.md             # Project documentation
├── my_list.txt           # List of training captions (required)
├── model.weights.h5      # Trained model weights (required)
├── templates/
│   └── index.html        # Web interface template (required)
```

---

## Requirements

- Python 3.8+
- Flask
- Pillow
- pandas
- tensorflow (tested with 2.x)
- numpy

You can install the dependencies with:

```bash
pip install Flask Pillow pandas tensorflow numpy
```

---

## Setup Instructions

1. **Clone or download this repository.**
2. **Ensure the following files are present in the project root:**
   - `my_list.txt` (a text file with one caption per line)
   - `model.weights.h5` (the trained model weights)
3. **Create a `templates` directory and add `index.html`**
   - The app expects a file at `templates/index.html` for the web UI.
4. **Install the required Python packages** (see above).
5. **Run the application:**

```bash
python app.py
```

6. **Open your browser and go to** [http://127.0.0.1:5000/](http://127.0.0.1:5000/) to use the app.

---

## Usage

- On the home page, upload an image file.
- The app will process the image and display a generated caption.

---

## File Descriptions

- **app.py**: Main application logic, model loading, and Flask routes.
- **my_list.txt**: List of captions used for tokenizer adaptation (must be present).
- **model.weights.h5**: Pre-trained model weights (must be present).
- **templates/index.html**: HTML template for the web interface.

---

## Customization

- To retrain or fine-tune the model, modify the code in `app.py` and provide your own dataset and weights.
- You can customize the web interface by editing `templates/index.html`.
