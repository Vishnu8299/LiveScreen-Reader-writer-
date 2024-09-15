# Screen Reader Application

## Overview

The **Screen Reader Application** allows you to capture a selected region of your screen, process the image using Optical Character Recognition (OCR), and extract any text contained within that region. The extracted text is saved to a `.txt` file for future reference.

This project uses the following technologies:
- **Python**
- **Tkinter** for the GUI
- **Pytesseract** for OCR (Tesseract OCR)
- **PIL (Pillow)** for image processing
- **mss** for screen capturing

## Features
- Capture full-screen images
- Select a specific region of the screen to process
- Extract text from the selected screen region using Tesseract OCR
- Save the extracted text as a `.txt` file with a timestamped filename

## Prerequisites

Before running the application, you need the following installed on your system:

1. **Python 3.x**
2. **Tesseract OCR**
   - Install Tesseract OCR on your machine.
   - For Windows, download and install Tesseract from [here](https://github.com/UB-Mannheim/tesseract/wiki).
   - Set the `tesseract_cmd` path in the script as shown below:
     ```python
     pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
     ```
   - Adjust the path according to where Tesseract is installed on your machine.
   
3. **Python Libraries**
   Install the required Python libraries using the following commands:
   ```bash
   pip install pytesseract
   pip install Pillow
   pip install mss
   ```

## How to Run

1. Clone the repository or download the code files.
2. Navigate to the project directory.
3. Run the application:
   ```bash
   python screen_reader.py
   ```
4. The application window will appear with a button labeled **"Capture Screen"**.
5. Click **"Capture Screen"** to capture the entire screen.
6. A new window will open, allowing you to select a region of the screen. Click and drag to define the area.
7. Once you've selected the region, the OCR process will extract the text from that area.
8. The extracted text will be printed in the console and saved to a `.txt` file in the same directory as the script.

## File Structure

```
.
├── screen_reader.py   # Main Python script
└── README.md          # This README file
```

## Usage Example

After running the application:

1. Click the **"Capture Screen"** button.
2. Select an area of your screen that contains text.
3. The extracted text will be printed in the console and saved as `extracted_text_<timestamp>.txt`.

Example output file:
```
extracted_text_20230915_123456.txt
```

## License

This project is licensed under the MIT License. Feel free to modify and distribute it.
