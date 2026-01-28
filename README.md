# s2t

We have a speech-to-text notebook that:

* Processes multiple audio files
* Splits each file into overlapping chunks
* Transcribes the chunks
* Merges transcriptions for each file
* Exports the full transcription into a single `.docx` per file

You just configure the parameters in the notebook and run it to generate transcriptions.

We don’t use standard GenAI pipelines (e.g., LangChain) since our focus is speech, not text—custom code is simpler and more efficient.

We use OpenAI s2t models for transcriptions.


## Environment Setup

We use [uv](https://github.com/astral-sh/uv) for Python env + lock management.

1. Open the folder in VS Code and select “Reopen in Container”.
2. Run `uv sync` inside the container to install packages.
3. Run the notebook

```

## Environment variables

Create a `.env` file in the project root and add required environment variables

```
OPENAI_API_KEY=your_openai_api_key_here
```
## Update Environment

After changing `pyproject.toml`, run:

```bash
uv sync
```
