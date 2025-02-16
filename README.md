# IDCardScanner
A Python-based College ID Card Scanner that uses OpenCV and Tesseract OCR for roll number authentication. The project captures an image, extracts the roll number via OCR, and verifies it against a predefined list. Integrated with Anvil Uplink for remote authentication. Built using Python, OpenCV, and Tesseract

College ID Card Scanner

This project is an ID Card Scanner for college authentication using Python, OpenCV, Tesseract OCR, and Anvil Uplink. It captures an image of the college ID card, extracts the roll number using Optical Character Recognition (OCR), and verifies the roll number against a predefined list for authentication.

Features

Live Camera Capture: Uses a webcam to take a photo of the ID card.

OCR Processing: Extracts the roll number from the scanned ID card using Tesseract OCR.

Authentication: Verifies the roll number against a predefined list of valid roll numbers.

Remote Integration: Uses Anvil Uplink for server-side processing.

Installation

To run this project, install the required dependencies:

pip install anvil-uplink
sudo apt install tesseract-ocr
pip install pytesseract

Usage

Capture an Image: Uses Google Colab's JavaScript to capture an image from the webcam.

OCR Processing: Converts the captured image to grayscale and extracts text using Tesseract OCR.

Authentication: Checks if the extracted roll number exists in the predefined list.

Server Integration: Anvil Uplink is used to handle remote authentication requests.

Code Overview

1. Installing Packages

Required dependencies:

!pip install anvil-uplink
!sudo apt install tesseract-ocr
!pip install pytesseract

2. Importing Libraries

import cv2
import pytesseract
import numpy as np
from PIL import Image
import anvil.server

3. Anvil Server Connection

anvil.server.connect("RWFIVIQ4QFHCNNSUGNW5A75Z-SVRWJCQTMVBAYHTV")

4. Capture Image from Webcam

Uses JavaScript in Google Colab to capture an image from the webcam.

5. Roll Number Authentication

Processes the captured image, extracts the roll number using OCR, and verifies it against a predefined list of valid roll numbers.

6. Server Authentication Endpoint

Anvil server callable function to process authentication requests.

Example Output

Authenticated

OR

Not Authenticated

Future Improvements

Implement a database to store valid roll numbers dynamically.

Improve OCR accuracy using advanced image preprocessing techniques.

Deploy as a standalone desktop/web application.

License

This project is licensed under the MIT License.

