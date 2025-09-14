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

Create the environment with:

```bash
conda env create -f environment.yml
```

Activate the environment:

```bash
conda activate s2t
```

## Environment variables

Create a `.env` file in the project root and add required environment variables

```
OPENAI_API_KEY=your_openai_api_key_here
```
## Update Environment

To update the environment after changing `environment.yml`:

```bash
conda env update -f environment.yml --prune
```
