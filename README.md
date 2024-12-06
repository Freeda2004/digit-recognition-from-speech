# digit-recognition-from-speech



# Speech-to-Text Project Using Wav2Vec2

## Project Description

This project uses the **Wav2Vec2 model** from **Hugging Face** to transcribe audio files in the **Free Spoken Digit Dataset (FSDD)**. The model converts speech into text, enabling **automatic speech recognition (ASR)**. The project also handles cases where audio files are recorded at an incorrect sample rate (such as 8 kHz), by **resampling** them to the required **16 kHz**.

### Features:
- **Speech Recognition** using pre-trained **Wav2Vec2**.
- **Resampling** of audio files to 16 kHz (if needed) before processing.
- **Transcription of digits** (0-9) from speech data.

---

## Installation

To set up the project, follow the steps below:

### Prerequisites:
- **Python 3.x** (Recommended: Python 3.6+)
- **pip** (Python package installer)

### Steps:
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository
   ```

2. Install the required dependencies:
   ```bash
   pip install transformers soundfile torch ffmpeg-python
   ```

3. Make sure you have **FFmpeg** installed on your system. If not, follow the installation instructions from [FFmpeg](https://ffmpeg.org/download.html).

---

## Dataset

This project uses the **Free Spoken Digit Dataset (FSDD)**, which contains recordings of digits (0-9) spoken by different people. You can download the dataset or clone it from [GitHub](https://github.com/Jakobovski/free-spoken-digit-dataset).

After downloading, place the **`recordings/`** folder in the project directory.

---

## Usage

### 1. Clone the Dataset

If you haven’t already, you need to download the **Free Spoken Digit Dataset**. You can do this with the following command:

```bash
git clone https://github.com/Jakobovski/free-spoken-digit-dataset.git
```

Make sure to place the `recordings/` folder in the root directory of the project.

### 2. Run the Transcription Script

You can run the transcription process for all the `.wav` files in the **`recordings/`** folder:

```bash
python transcribe.py
```

This will:
- Process the audio files in the `recordings/` folder.
- Resample the files to **16 kHz** if the sample rate is different.
- Transcribe the speech data and print the transcriptions to the console.

### Example of transcriptions:
```
0_jackson_0.wav: zero
0_jackson_1.wav: zero
1_jackson_0.wav: one
...
```

---

## Project Structure

Here’s a simple breakdown of the project directory:

```
/speech-to-text-project
  README.md                    # Project documentation
  /recordings                   # Folder containing .wav audio files
  /recordings/resampled         # Folder containing resampled audio files (for 16 kHz)
  transcribe.py                 # Main script for transcribing audio
  requirements.txt              # List of Python dependencies
```

---

## Expected Output

After running the transcription script, you should expect to see the following format:

```
Processing file: speech_dataset/recordings/0_jackson_0.wav
Transcription for 0_jackson_0.wav: zero
Processing file: speech_dataset/recordings/1_jackson_0.wav
Transcription for 1_jackson_0.wav: one
...
```

If there are any issues with the sample rate, those files will be skipped with an appropriate message:
```
Skipping 0_jackson_0.wav: Unsupported sample rate 8000
```

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- The **Wav2Vec2** model was developed by [Hugging Face](https://huggingface.co/).
- The **Free Spoken Digit Dataset** is maintained by [Jakobovski](https://github.com/Jakobovski/free-spoken-digit-dataset).
```

---

3. **Save the `README.md` File**:
   - After pasting the content, **save the file**. Make sure it’s saved with the name `README.md` (not just `README`).

4. **Commit the README to GitHub**:
   - If you're using **Git** and want to push the `README.md` file to your GitHub repository, follow these steps:
   
   - In your project folder, open the **terminal** (or Git Bash).
   
   - If you haven’t already initialized Git in your project, run the following:
     ```bash
     git init
     ```

   - Stage the `README.md` file:
     ```bash
     git add README.md
     ```

   - Commit the changes:
     ```bash
     git commit -m "Add README file"
     ```

   - Push the file to your **GitHub repository**:
     ```bash
     git remote add origin https://github.com/your-username/your-repository.git
     git push -u origin master
     ```

---

### **Summary**
- **Create the `README.md`** file in the root of your project folder.
- **Paste the provided content** into the file.
- **Save the file**, and if using Git, **commit and push** it to your GitHub repository.

This will ensure that your **README** is added to the root of your project and displayed on GitHub. Let me know if you need further help!
