
# Image Captioning AI App

This project is an AI-powered image captioning application built using OpenAI's GPT model and Gradio for the user interface. The app generates descriptive captions and relevant tags for uploaded images.

## Features

- Automatically generates a detailed caption for any uploaded image.
- Provides 10-15 relevant tags for each image.
- Interactive user interface built with Gradio.
- Includes example images for quick testing.

## Requirements

Make sure you have the following installed:

- Python 3.7 or higher
- OpenAI Python library
- Gradio Python library

## Installation

1. Clone the repository or copy the script.

   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. Install the required Python packages:

   ```bash
   pip install openai gradio
   ```

3. Download the example images:

   ```bash
   mkdir images
   wget -q -O images/cheetah1.jpg https://github.com/gradio-app/gradio/raw/main/demo/image_mod/images/cheetah1.jpg
   wget -q -O images/lion.jpg https://github.com/gradio-app/gradio/raw/main/demo/image_mod/images/lion.jpg
   wget -q -O images/tower.jpg https://github.com/gradio-app/gradio/raw/main/demo/image_mod/images/tower.jpg
   ```

## Configuration

1. Obtain your OpenAI API key from [OpenAI](https://platform.openai.com/).

2. Update the script to include your OpenAI API key:

   ```python
   from getpass import getpass
   import openai

   openai.api_key = getpass("Please enter your OpenAI API Key: ")
   ```

## Usage

Run the script to start the application:

```bash
python app.py
```

The Gradio interface will launch and provide a shareable link (e.g., `https://<your-app-url>.gradio.live`). Use this link to access the application.

## How It Works

1. Upload an image through the Gradio interface.
2. The app encodes the image in base64 format and sends it to OpenAI's GPT model.
3. The model generates a descriptive caption and relevant tags.
4. The output is displayed in the Gradio interface.

## Example Output

For the image `lion.jpg`, the app generates:

**Caption:**
> A majestic lion and lioness rest together atop a large rock, illustrating their serene yet powerful presence in the wild.

**Tags:**
> #Lion #Lioness #Wildlife #Nature #Animals #BigCats #Savannah #KingOfTheJungle #Predator #Majestic #Serenity #WildlifePhotography #CatsOfInstagram #NatureLovers #AnimalKingdom

## Code Overview

### Key Functions

- **encode_image(image_path)**
  Encodes the image into base64 format for processing.

- **caption_image(image_path)**
  Sends the encoded image to OpenAI's GPT model and retrieves the caption and tags.

### Gradio Interface

The app uses Gradio to create an interactive UI with the following:
- An image input field.
- A text output field.
- Example images preloaded for testing.

## Example Images

The following example images are included for testing:
- `cheetah1.jpg`
- `lion.jpg`
- `tower.jpg`

## Deployment

To deploy the app permanently:

1. Use the shareable Gradio link generated when running the app.
2. For permanent hosting, deploy to Hugging Face Spaces:

   ```bash
   gradio deploy
   ```

## License

This project is licensed under the MIT License. Feel free to use and modify it as needed.

## Acknowledgements

- [OpenAI](https://openai.com/) for the GPT API.
- [Gradio](https://gradio.app/) for the user interface library.

---

Feel free to contact [Your Name/Email] for additional support or questions.
