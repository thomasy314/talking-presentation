# Talking Presentation

This tool is designed to quickly create presentation slides with accompanying audio from a simple text file, making it easier to prepare presentations with pre-recorded narration. The audio is generated from Azure [Cognitive Speech Service](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/index-text-to-speech). 

## Prerequisites

- Python 3.x
- An Azure account with access to the Cognitive Speech Service

## Setup

### 1. Install Python Dependencies

```sh
pip install -r requirements.txt
```

### 2. Azure Prerequisites

Follow the prerequisites on the Azure Cognitive Speech Service [quickstart page](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/get-started-text-to-speech?tabs=linux%2Cterminal&pivots=programming-language-python#prerequisites) to set up your account and obtain a key and region for the speech SDK.

### 3. Set Up Environment

Follow the [Set environment variables](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/get-started-text-to-speech?tabs=linux%2Cterminal&pivots=programming-language-python#set-environment-variables) guide to pass the key and region information to the program securely.

## Usage

```sh
python3 main.py --input-file [text file] --output-files-prefix [output file prefix]

# Example
python3 main.py --input-file dino-presentation-text.txt --output-files-prefix dino-presentation
```

### Arguments

- `--input-file`: The path (relative to the current directory) to the input text file. Each new line in the file will indicate a new slide with audio to be created.

    **Example:**
    ```
    Fizz
    Buzz
    Fizz Buzz
    ```

    The above file will create a presentation with 3 slides and 3 audio files.

- `--output-files-prefix`: The prefix used for creating the presentation and audio files. All files are output to the `output` subfolder.

    **Example:**
    `--output-files-prefix dino-presentation` will create the following files assuming 3 slides are created:
    - `output/dino-presentation.pptx`
    - `output/dino-presentation-0.wav`
    - `output/dino-presentation-1.wav`
    - `output/dino-presentation-2.wav`

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss any changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact Information

For questions or support, please contact [your email or GitHub profile].