# FastAPI Transformers inference boilerplate

This project is a sample FastAPI application that uses `openai/clip-vit-base-patch32` model from [Hugging Face](https://huggingface.co/openai/clip-vit-base-patch32) for inference.

## Getting Started

### Prerequisites

- Python 3.10

### Installation

1. Clone the repository:
```
git clone https://github.com/vctrmn/FastAPI-Inference-Boilerplate.git
```

2. Install the dependencies
```
pip install -r requirements.txt
```

### Running the Application

3. Start the application
```
python run.py
```

4. Open [http://localhost:8000/docs](http://localhost:8000/docs) in your browser to view the Swagger UI.

### Running the Tests

To run the tests, execute the following command:
```
pytest
```

## Usage

### Zero image classification

To classify the image with its input labels, send a POST request to the `/api/classifier` endpoint with the following payload:
```json
{
    "imageUrl": "https://aaaaaa.com/sdasd.jpg",
    "labels": ["xxxx","yyyy","zzzz"]
}
```

The response will be a JSON object with the following structure:
```json
[
    {
        "label": "xxxx",
        "score": 95.54687354
    },
    {
        "label": "yyyy",
        "score": 1.234443184
    },
    {
        "label": "zzzz",
        "score": 3.908742123
    }
]
```

## Contributing

Contributions are welcome! Please open an issue or pull request for any changes.

## License

This project is licensed under the MIT License. See LICENSE for more information.