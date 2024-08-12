# OCR Application

This is a simple Optical Character Recognition (OCR) application built using Python. The application allows users to select an image file, preprocess it, and extract the text content using the OCR.Space API. The extracted text is then displayed in a graphical user interface (GUI) built with Tkinter.

## Features

- **Image Preprocessing**: Converts the image to grayscale, applies Gaussian blur, and uses Otsu's thresholding to prepare the image for OCR.
- **OCR Extraction**: Uses the OCR.Space API to extract text from the preprocessed image.
- **GUI Interface**: A user-friendly interface for selecting images and displaying the OCR results.

## Requirements

- Python 3.x
- OpenCV (`cv2`)
- NumPy
- Requests
- Tkinter (usually included with Python)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/ocr-application.git
    ```

2. Navigate to the project directory:

    ```bash
    cd ocr-application
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

    If you don't have a `requirements.txt` file, you can manually install the dependencies:

    ```bash
    pip install opencv-python-headless numpy requests
    ```

## Usage

1. Run the application:

    ```bash
    python ocr_application.py
    ```

2. A GUI window will appear. Click on the "Open Image" button to select an image file.

3. The application will preprocess the image and send it to the OCR.Space API.

4. The extracted text will be displayed in a new window.

## Configuration

- **API Key**: The OCR.Space API requires an API key. Replace the `api_key` parameter in the `ocr_space_api` function with your own key. You can obtain a free API key from [OCR.Space](https://ocr.space/ocrapi).

```python
def ocr_space_api(image_path, api_key='your_api_key_here'):
