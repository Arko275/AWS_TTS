# AWS_TTS
Certainly! Here's a detailed README file for your GitHub repository:

---

# Private Text-to-Speech Application

This project leverages Amazon Polly to convert text into speech. It provides an easy-to-use graphical user interface (GUI) built with Tkinter, allowing users to input text and have it spoken aloud using Amazon Polly's text-to-speech service.

## Features

- **Text Input**: A text area for users to input the text they want to convert to speech.
- **Text-to-Speech Conversion**: Utilizes Amazon Polly to convert text to speech.
- **MP3 Output**: Saves the converted speech as an MP3 file in the system's temporary directory.
- **Cross-Platform Compatibility**: Works on Windows and other platforms with appropriate adjustments.

## Prerequisites

- **Python 3.x**: Ensure Python is installed on your system.
- **AWS Account**: An active AWS account with access to Amazon Polly.
- **AWS Credentials**: Configured AWS credentials (e.g., via AWS CLI or environment variables).

## Installation

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/yourusername/private-text-to-speech.git
    cd private-text-to-speech
    ```

2. **Install Required Packages**:
    ```sh
    pip install boto3
    ```

3. **Configure AWS Credentials**:
    Ensure your AWS credentials are set up. You can configure these using the AWS CLI:
    ```sh
    aws configure
    ```
    Alternatively, you can set the environment variables `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`.

## Usage

1. **Run the Application**:
    ```sh
    python polly.py
    ```

2. **Enter Text**:
    In the text area, input the text you want to convert to speech.

3. **Convert Text to Speech**:
    Click the "Read" button to convert the text to speech. The application will save the speech as an MP3 file in the system's temporary directory and play it (if on Windows).

## Code Overview

- **polly.py**: The main script containing the application logic and GUI setup.

### Main Components

- **Tkinter GUI**: Provides a user-friendly interface with a text input area and a "Read" button.
- **Amazon Polly Integration**: Uses Boto3 to interact with Amazon Polly for text-to-speech conversion.

### Error Handling

- If the selected voice does not support the `neural` engine, the application will handle the error and display a message.
- Any IOError during file operations or AWS Polly interactions are caught and logged.

## Contributing

Contributions are welcome! Please fork the repository and submit pull requests for any features or bug fixes.

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push the branch.
4. Create a pull request detailing your changes.

## Acknowledgements

- [Amazon Polly](https://aws.amazon.com/polly/) for providing the text-to-speech service.
- [Tkinter](https://docs.python.org/3/library/tkinter.html) for the GUI framework.


