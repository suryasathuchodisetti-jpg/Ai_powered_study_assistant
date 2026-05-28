# Ai_powered_study_assistant
Initial commit - AI Study Assistant using Gemini API
# AI Powered Study Assistant

An AI-powered study assistant built using Python, Google Colab, and the Gemini API. This project can answer academic questions, explain concepts in simple terms, and assist students with learning tasks using Large Language Models (LLMs).

---

## Features

* AI-powered academic question answering
* Uses Gemini 2.5 Flash model
* Secure API key handling with Colab Secrets
* Beginner-friendly Python implementation
* Runs directly in Google Colab
* Easy to customize and expand

---

## Technologies Used

* Python
* Google Colab
* Gemini API
* google-genai SDK

---

## Project Structure

```text
ai-powered-study-assistant/
│
├── ai_powered_study_assistant.ipynb
├── README.md
├── requirements.txt
└── screenshots/
```

---

## Installation

Install dependencies:

```bash
pip install -U google-genai
```

Or using requirements.txt:

```bash
pip install -r requirements.txt
```

---

## Setup API Key

1. Go to Google AI Studio
2. Create a Gemini API key
3. Open Google Colab
4. Click the key icon in the sidebar
5. Add a new secret:

```text
Name: GEMINI_API_KEY
Value: Your API Key
```

6. Enable notebook access

---

## Full Working Code

```python
from google import genai
from google.colab import userdata

# Access API key
api_key = userdata.get("GEMINI_API_KEY")

# Initialize Gemini client
client = genai.Client(api_key=api_key)

# Study assistant function

def study_assistant(user_prompt):

    response = client.models.generate_content(
        model="gemini-2.5-flash",
        contents=user_prompt
    )

    return response.text

# Ask a question
user_question = input()

# Get response
output = study_assistant(user_question)

# Print answer
print(output)
```

---

## Example Output

**Input:**

```text
Explain Generative AI in simple terms
```

**Output:**

```text
Generative AI is a type of artificial intelligence that can create new content such as text, images, music, or code by learning patterns from existing data.
```

---

## Future Improvements

* Chat history support
* PDF summarizer
* Voice assistant
* Quiz generator
* Flashcard creator
* Streamlit web app
* OCR for handwritten notes
* Multi-language support

---


---

## requirements.txt

```text
google-genai
```

---

## Author

Developed as a beginner AI project to learn API integration, prompt engineering, and LLM application development.

