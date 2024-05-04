# Video Chat and File Transfer Application

This project implements a video chat and file transfer application using socket programming in Python. It enables communication between users over a local network.

## Technical Overview

### 1. Video Chat

- **Video Streaming**: The application captures video frames from the user's camera using OpenCV. The frames are then encoded and transmitted over the network to the recipient.
  
- **Socket Programming**: The video streaming functionality is implemented using sockets. A separate thread is used to handle each video stream, ensuring real-time transmission.

### 2. File Transfer

- **File Selection**: Users can select files from their local directory using the graphical user interface (GUI). Both text and binary files are supported for transfer.

- **Socket Communication**: When a file is selected for transfer, the application establishes a connection with the recipient using sockets. It then sends the file data over the network.

### 3. Graphical User Interface (GUI)

- **Tkinter Framework**: The GUI is built using the Tkinter framework, which provides a set of tools for creating graphical interfaces in Python.

- **User Interaction**: The GUI allows users to initiate video calls by selecting a contact from the user list. It also provides options for selecting files and initiating file transfers.

## Technical Implementation

### 1. Initialization

- **User Information**: User information is read from a text file (`User/User_list.txt`) and stored in a dictionary for easy access during communication.

- **Socket Setup**: The application sets up sockets for both video streaming and file transfer. The video socket listens on a specified port for incoming connections.

### 2. Video Streaming

- **Capture and Processing**: Video frames are captured from the user's camera using OpenCV. Each frame is resized and converted to the appropriate format for transmission.

- **Multi-Threading**: Video streaming is implemented using multi-threading to ensure smooth transmission. Each video stream is handled by a separate thread.

### 3. File Transfer

- **File Selection**: Users can select files using the GUI's file picker widget. The selected file's path is then passed to the file transfer function.

- **Transfer Protocol**: For text files, the application reads the file line by line and sends each line as a string over the network. For binary files, the file data is read and sent in chunks.

### 4. GUI Interaction

- **User Interface Design**: The GUI provides a user-friendly interface for initiating video calls, selecting files, and monitoring file transfer progress.

- **Button Actions**: Callback functions are defined for GUI buttons to handle user interactions such as initiating video calls and sending files.

## Dependencies

- Python 3.12
- OpenCV
- Tkinter
- PIL (Python Imaging Library)

