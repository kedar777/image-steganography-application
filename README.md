# Image Steganography Application

This Python script implements a simple image steganography application using the Tkinter GUI library for the user interface and the stegano library for encoding and decoding messages within image files. The application allows users to encode a message into an image and decode a hidden message from an image.

## Dependencies

- `subprocess`: For starting a new Python process.
- `tkinter`: GUI library for creating the application interface.
- `tkinter.font`: Module for setting font properties in Tkinter.
- `tkinter.messagebox`: Module for displaying message boxes in Tkinter.
- `tkinter.filedialog`: Module for opening file dialogs in Tkinter.
- `PIL`: Python Imaging Library for image manipulation.
- `stegano`: Library for steganography operations, including hiding and revealing messages in images.

## Usage

### Main Program

1. The main program creates a fullscreen Tkinter window with three buttons: "Encode," "Decode," and "EXIT."
2. Clicking the "Encode" button opens a new window for encoding a message into an image.
3. Clicking the "Decode" button opens a new window for decoding a hidden message from an image.
4. The "EXIT" button closes the main window and exits the application.

### Encoding Window (`encode` function)

1. The encoding window allows users to select an image file, choose the format (JPEG or PNG) for the output image, enter a message, and specify the output file name.
2. Clicking the "Openfile" button opens a file dialog for selecting an image file.
3. Users can choose the output image format (JPEG or PNG) using radio buttons.
4. Enter a message to be encoded in the "Enter message" entry.
5. Enter the desired file name for the output image in the "File Name" entry.
6. Clicking the "ENCODE" button triggers the encoding process.
7. The encoded image is saved in the specified format, and a success or failure message is displayed.
8. Clicking the "Back" button returns to the main menu.

### Decoding Window (`decode` function)

1. The decoding window allows users to select an image file and choose the format (JPEG or PNG) for decoding.
2. Clicking the "Openfile" button opens a file dialog for selecting an image file.
3. Users can choose the input image format (JPEG or PNG) using radio buttons.
4. Clicking the "DECODE" button triggers the decoding process.
5. The hidden message is revealed, and it is displayed in a label.
6. Clicking the "Back" button returns to the main menu.

### Screenshots

#### Encoding Window

![Encode Window](screens/encode%20screen.png)

#### Decoding Window

![Decode Window](screens/decode%20screen.png)

### Closing the Application

1. Clicking the "EXIT" button in the main window closes the application.

## Notes

- The steganography operations are performed using the `stegano` library, specifically the `lsb` module for PNG images and the `exifHeader` module for JPEG images.
- The application uses multiple Tkinter windows for different functionalities.
- The application utilizes image files ("bg1.jpg" and "bg2.jpg") for the background of the Tkinter windows.

**Note:** It's important to ensure that the required dependencies (`subprocess`, `tkinter`, `PIL`, `stegano`) are installed before running the script. Additionally, the stegano library should be installed using `pip install stegano`.
