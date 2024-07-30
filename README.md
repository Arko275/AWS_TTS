# AWS_TTS
This application uses Amazon Polly to convert text to speech. It provides a simple graphical user interface (GUI) using Tkinter, where users can input text and convert it to speech.

Features
Text input area for entering the text to be converted to speech.
Button to trigger the text-to-speech conversion.
Uses Amazon Polly for high-quality text-to-speech synthesis.
Supports both neural and standard engines in Amazon Polly.
Saves the generated speech as an MP3 file.
Prerequisites
Python 3.x
AWS account with access to Amazon Polly
AWS credentials configured (e.g., through AWS CLI or environment variables)
Installation
Clone the repository:

sh
Copy code
git clone https://github.com/yourusername/private-text-to-speech.git
cd private-text-to-speech
Install required packages:

sh
Copy code
pip install boto3
Configure AWS credentials:

Ensure your AWS credentials are set up, either through the AWS CLI or by setting the environment variables AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY. You can also set up a profile for polly_user in your AWS credentials file.

Usage
Run the application:

sh
Copy code
python polly.py
Enter text:

Enter the text you want to convert to speech in the text area of the application.

Convert to speech:

Click the "Read" button to convert the text to speech. The application will save the generated speech as an MP3 file in the system's temporary directory and play it if you are using Windows.

Code Overview
polly.py: Main script containing the application logic and GUI setup.
Main Components
Tkinter GUI: Provides a text input area and a button to trigger text-to-speech conversion.
Amazon Polly Integration: Uses Boto3 to interact with Amazon Polly for text-to-speech synthesis.
Error Handling
The application handles cases where the selected voice does not support the neural engine by falling back to the standard engine.
Any errors during the file writing process or AWS Polly interaction are caught and displayed in the console.
