# MedGuide-AI

MedGuide-AI is a Python application for building a medical guidance assistant with Flask, LangChain, OpenAI, Pinecone, PDF ingestion, and sentence-transformer embeddings.

The repository is currently a scaffold: the folder structure and dependencies are in place, but the main application files are still mostly empty.

## Project Structure

```text
MedGuide-AI/
├── app.py
├── requirements.txt
├── setup.py
├── README.md
├── .env
├── src/
│   ├── __init__.py
│   ├── helper.py
│   └── prompt.py
└── research/
    └── medguide-notebook.ipynb
```

## Requirements

- Python 3.10 or newer
- Conda
- `pip`
- Bash

## Installation

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd MedGuide-AI
```

### 2. Create and activate a Conda environment

```bash
conda create -n medguide python=3.10 -y
conda activate medguide
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Install the project in editable mode

```bash
pip install -e .
```

This lets you update local source code without reinstalling the package each time.

## Environment Variables

Create or update `.env` with the keys your app will need.

Example:

```env
OPENAI_API_KEY=your_openai_api_key
PINECONE_API_KEY=your_pinecone_api_key
PINECONE_ENVIRONMENT=your_pinecone_environment
PINECONE_INDEX_NAME=your_index_name
```

Depending on how you build the app, you may also want:

```env
FLASK_APP=app.py
FLASK_ENV=development
```

## Commands

### Install dependencies

```bash
pip install -r requirements.txt
```

### Install local package in editable mode

```bash
pip install -e .
```

### Upgrade pip

```bash
python -m pip install --upgrade pip
```

### Run the Flask app

Use this once `app.py` contains a Flask application:

```bash
export FLASK_APP=app.py
export FLASK_ENV=development
flask run
```

Alternative:

```bash
python app.py
```

Use the `python app.py` command only if your file defines the standard entry point:

```python
if __name__ == "__main__":
    app.run(debug=True)
```

### Run a Jupyter notebook

```bash
jupyter notebook
```

Then open:

```text
research/medguide-notebook.ipynb
```

### Freeze dependencies

```bash
pip freeze > requirements.txt
```

## Current Dependencies

- `langchain`: framework for building LLM workflows
- `flask`: lightweight web app framework
- `sentence-transformers`: text embedding models
- `pypdf`: PDF text extraction
- `python-dotenv`: load environment variables from `.env`
- `langchain-pinecone`: Pinecone integration for LangChain
- `langchain-openai`: OpenAI integration for LangChain
- `langchain-community`: community integrations for LangChain

## Development Notes

- The setup in this repository has been done with Conda and Bash-style commands.
- `app.py`, `src/helper.py`, `src/prompt.py`, and `src/__init__.py` are currently empty.
- The project structure is ready, but the main logic still needs to be implemented.
- If `pip install -r requirements.txt` fails, check the last line of `requirements.txt`. Editable installs should be written as `-e .`.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
