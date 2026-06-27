# Multi-Input Model for OCR

A multimodal Optical Character Recognition (OCR) system that combines visual document understanding with natural language prompts to extract structured text from images. The project demonstrates how modern vision-language models can leverage both image input and textual instructions to improve OCR accuracy and flexibility across different document types.

---

## Overview

Traditional OCR systems focus solely on recognizing text from images. This project extends that workflow by incorporating multiple input modalities, allowing the model to understand both:

- Document images
- User-provided text prompts or instructions

This approach enables more context-aware document understanding, making it suitable for extracting specific information rather than simply transcribing all visible text.

---

## Features

- Multi-input inference pipeline
- OCR from images using a vision-language model
- Prompt-guided information extraction
- Structured text generation
- Modular preprocessing and inference workflow
- Easily extensible to different document formats

---

## Use Cases

- Receipt digitization
- Invoice processing
- Identity document parsing
- Form extraction
- Business card digitization
- Academic document analysis
- General document OCR

---

## Project Structure

```text
Multi-Input-Model-For-OCR/
│
├── app/                 # Application entry point
├── models/              # Model loading and configuration
├── utils/               # Image preprocessing utilities
├── inference/           # OCR inference pipeline
├── examples/            # Sample inputs
├── requirements.txt
└── README.md
```

*(Directory names may vary slightly depending on the current implementation.)*

---

## How It Works

1. An image containing text is provided.
2. The image is preprocessed for optimal recognition.
3. A textual instruction or prompt is supplied alongside the image.
4. The multimodal model jointly processes both inputs.
5. The model returns the requested textual information in a structured format.

```
Image
   │
   ▼
Image Preprocessing
   │
   ├─────────────┐
   ▼             ▼
Image Encoder   Text Prompt
       │         │
       └────┬────┘
            ▼
 Vision-Language Model
            │
            ▼
 Structured OCR Output
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/kinola-IQ/Multi-Input-Model-For-OCR.git

cd Multi-Input-Model-For-OCR
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it:

Windows

```bash
.venv\Scripts\activate
```

Linux/macOS

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Usage

Run the application:

```bash
python app.py
```

or

```bash
python main.py
```

depending on the project entry point.

Example workflow:

```python
image = "sample_document.png"

prompt = """
Extract the invoice number,
date,
vendor name,
and total amount.
"""

result = model.predict(image, prompt)

print(result)
```

---

## Example Prompt

```
Extract all handwritten text from this document.

Return the output as JSON with:

- Name
- Address
- Phone Number
- Email
```

---

## Example Output

```json
{
  "name": "John Doe",
  "address": "12 Main Street",
  "phone": "+1 555-123-4567",
  "email": "john@example.com"
}
```

---

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Vision-Language Models
- Pillow
- NumPy

---

## Future Improvements

- PDF support
- Batch document processing
- Table extraction
- Layout-aware document understanding
- Confidence score visualization
- REST API deployment
- Docker support
- Streamlit web interface

---

## Learning Objectives

This project explores:

- Multimodal AI systems
- Vision-language models
- Prompt-guided OCR
- Document understanding
- Information extraction
- AI application development

---

## Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push the branch.
5. Open a Pull Request.

---

## License

This project is licensed under the MIT License.

---

## Author

**Omolayo Akinola**

Applied AI Engineer

GitHub: https://github.com/kinola-IQ