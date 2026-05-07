# Workshop Data Collection/Annotation & Inferences with LLMs in Social Sciences

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20073016.svg)](https://doi.org/10.5281/zenodo.20073016)

This repository contains the code and slides for our workshop on data collection/annotation and inference with Large Language Models. The materials on this page are [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) licensed.

![cc](https://mirrors.creativecommons.org/presskit/icons/cc.svg) ![by](https://mirrors.creativecommons.org/presskit/icons/by.svg)

More information can be found on the website [here](https://sodascience.github.io/workshop_llm_data_collection/).

<img src="img/llm_data_collection.png" alt="SoDa logo" width="100%"/>

## Technical details
- No previous experience with LLMs is required.
- `R` or `python` programming knowledge is desired but not required.
- In python we will use [`langchain`](https://python.langchain.com/docs/introduction/), in R we will use [`ellmer`](https://ellmer.tidyverse.org/) to interact with LLMs.

## Preparation (API keys)
You will need an API key for the respective provider you plan to use.

- **Hugging Face Inference API:**
	1. Create an account at https://huggingface.co/.
	2. Go to https://huggingface.co/settings/tokens and create a new access token.

- **OpenAI:**
	1. Create an account at https://platform.openai.com/.
	2. Create an API key at https://platform.openai.com/api-keys.

- **Groq:**
	1. Create an account at https://console.groq.com/.
	2. Create an API key in the Groq console.

- **SURF AI Hub**:
	1. It is in pilot phase and requires an [application](https://servicedesk.surf.nl/wiki/spaces/WIKI/pages/222464732/Onboarding#Onboarding-Step1%3AShowinterest) and approval process to get access.
	2. Once you have access, you can create an API key at https://willma.surf.nl/.

Save your API keys in a safe place. The notebooks will prompt you to enter the keys at runtime.

## Slides
- Full workshop slides (v2026.01.23): [`Download`](./slides/soda_llm_workshop_slides.pdf)
- ODISSEI 2025 workshop slides: [`Download`](./slides/soda_llm_workshop_odissei_25_slides.pdf)

## Full Workshop Schedule

| Time  | Title                                | Resource                                                                            |
| :---- | :----------------------------------- | :------------------------------------------------------------------------------------------- |
| 09:30 | LLM fundamentals for Social Sciences |                                                  |
| 11:00 | Coffee break                         | Coffee is provided!                                                                          |
| 11:20 | Data collection/annotation with LLMs | [`python`](https://colab.research.google.com/github/sodascience/workshop_llm_data_collection/blob/main/notebooks/llm_data_collection_py.ipynb), [`R`](https://colab.research.google.com/github/sodascience/workshop_llm_data_collection/blob/main/notebooks/llm_data_collection_R.ipynb) |
| 12:30 | Break                                | Lunch is provided!                                                                           |
| 13:15 | Inference with LLM annotations    | [`python`](https://colab.research.google.com/github/sodascience/workshop_llm_data_collection/blob/main/notebooks/llm_inferential_regression_py.ipynb), [`R`](https://colab.research.google.com/github/sodascience/workshop_llm_data_collection/blob/main/notebooks/llm_inferential_regression_R.ipynb)     |
| 14:30 | Conclusion & Q&A                     |                                                                                              |

Methods and software for inference with measurement error correction: [sodascience/social_science_inferences_with_llms](https://github.com/sodascience/social_science_inferences_with_llms).

## Additional Resources
### Tutorial Paper
Read and cite our tutorial paper (preprint):
- Fang, Q., Bernardo, J. G., & van Kesteren, E. J. (2026). A Methodological Guide on Using Large Language Models for Text Annotation in the Social Sciences and Humanities with Python and R. arXiv preprint arXiv:2604.09638.
- [`Download`](https://arxiv.org/abs/2604.09638) from arXiv

### Guide to LLM Computing Infrastructure in the Netherlands
- [Link](https://sodascience.github.io/soda_llm_infra_guide/)

## [Optional] Run Locally with uv and Python
If you plan to run the Python notebooks locally, we recommend using [`uv`](https://github.com/astral-sh/uv) to set up a clean Python environment. You can also use `uv` to launch Jupyter Lab or Notebook.

1. Clone the repository:
	- `git clone https://github.com/sodascience/workshop_llm_data_collection.git`
	- `cd workshop_llm_data_collection`
2. Create and sync the environment:
	- `uv venv`
	- `uv sync`
3. Start Jupyter:
	- `uv run jupyter lab`  (or `uv run jupyter notebook`)

If you use a different environment manager, make sure the dependencies in `pyproject.toml` are installed before running the notebooks.

## Contact

This project is developed and maintained by the [ODISSEI Social Data Science (SoDa)](https://odissei-soda.nl/) team.

<img src="img/soda_logo.png" alt="SoDa logo" width="250px"/>

Do you have questions, suggestions, or remarks? File an [issue](https://github.com/sodascience/workshop_llm_data_collection/issues) or feel free to contact [Qixiang Fang](https://github.com/fqixiang).
