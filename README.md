# 📖 Story Generator

A short-story generator that turns a genre + keywords + tone into an original
short story, using prompt engineering (role + constraints) on top of an
open-source text-generation model (`distilgpt2` from Hugging Face).

## How it works
1. User inputs are wrapped into a role + constraint prompt (see `build_prompt`).
2. The prompt is passed to a Hugging Face `text-generation` pipeline.
3. The generated continuation is returned as the story.

## Run it
Open `Story_Generator.ipynb` in **Google Colab** (works fully in a mobile
browser — no install needed):

1. Go to https://colab.research.google.com
2. `File > Upload notebook` → select `Story_Generator.ipynb`
   (or open directly from GitHub once this repo is pushed: `File > Open notebook > GitHub` and paste the repo URL)
3. `Runtime > Run all`
4. Edit the `genre`, `keywords`, and `tone` fields in the last cell and re-run to generate a new story.

## Tech stack
- Python
- Hugging Face `transformers` (`distilgpt2`)
- Runs on free Colab CPU — no API key required

## Possible improvements
- Swap in a larger/hosted model (GPT-4, Gemini, Llama) via API for higher-quality output
- Add genre-specific few-shot examples to steer style more precisely
- Add a Gradio/Streamlit UI for a shareable web app
