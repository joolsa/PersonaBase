# Persona Datasets

Below is a summary of persona datasets used in HCI, NLP/ML, and related research. These datasets are open source datasets available online.

| Category            | Sub-category   | ID   | Dataset name           | Year released | Description | Realness   | Domain type | Link |
|---------------------|----------------|------|------------------------|---------------|-------------|------------|-------------|------|
| Persona Development | —              | DS01 | YouTube Audience       | 2011 | Demographic user segments with 12,347 features across regions, genders, and age groups. | real       | HCI     | [Dataset link](https://github.com/joolsa/Persona-Generation) |
| Persona Development | —              | DS03 | Predictive-Personas    | 2023 | Survey responses from pet owners on demographics, lifestyles, and product preferences. | real       | HCI     | [Dataset link](https://github.com/ShihChu/Predictive-Personas) |
| Personas            | Dialogue       | DS02 | Persona-Chat           | 2018 | Crowdsourced conversations with persona profiles (4–5 sentences). | real       | NLP/ML  | [Dataset link](https://huggingface.co/datasets/awsaf49/persona-chat) |
| Personas            | Dialogue       | DS04 | CharacterChat          | 2023 | 10K conversations between MBTI characters with rich persona profiles. | synthetic  | NLP/ML  | [Dataset link](https://github.com/morecry/CharacterChat) |
| Personas            | Dialogue       | DS05 | Synthetic-Persona-Chat | 2023 | Synthetic extension of Persona-Chat with 5,648 personas and 11,001 conversations. | synthetic  | NLP/ML  | [Dataset link](https://github.com/google-research-datasets/Synthetic-Persona-Chat) |
| Personas            | Dialogue       | DS12 | AlignX                 | 2025 | 1.2M responses for personalized alignment, with personas spanning 90 dimensions. | synthetic  | NLP/ML  | [Dataset link](https://github.com/JinaLeejnl/AlignX) |
| Personas            | Deepfakes      | DS06 | Deepfake personas      | 2023 | Synthetic deepfake video personas created with Synthesia (Ashley, John, Isabel, Pablo). | synthetic  | HCI     | [Dataset link](https://github.com/danial-amin/deepfake-personas) |
| Personas            | Descriptions   | DS07 | FinePersonas           | 2024 | 21M synthetic persona descriptions with domains, skills, and interests. | synthetic  | NLP/ML  | [Dataset link](https://huggingface.co/datasets/argilla/FinePersonas-v0.1) |
| Personas            | Descriptions   | DS08 | PERSONA                | 2024 | 1.5K synthetic personas grounded in US Census demographics and traits. | synthetic  | NLP/ML  | [Dataset link](https://huggingface.co/datasets/SynthLabsAI/PERSONA) |
| Personas            | Descriptions   | DS09 | Personas-addicted      | 2024 | 450 synthetic personas modeling different addiction types (social media, gambling, etc.). | synthetic  | HCI     | [Dataset link](https://bit.ly/LLM-personas-data) |
| Personas            | Descriptions   | DS10 | Nemotron-Personas      | 2025 | 100K personas with six persona types and 16 contextual attributes. | synthetic  | NLP/ML  | [Dataset link](https://huggingface.co/datasets/nvidia/Nemotron-Personas) |
| Personas            | Descriptions   | DS11 | PersonaHub             | 2025 | 1B diverse synthetic personas with detailed knowledge and skills. | synthetic  | NLP/ML  | [Dataset link](https://huggingface.co/datasets/proj-persona/PersonaHub) |



---

## How to Use GitHub Datasets
1. Clone the repository:
   ```bash
   git clone <repo_url>
   cd <repo_name>
   ```
2. Load files (CSV/JSON/JSONL) using Python:
   ```python
   import pandas as pd
   df = pd.read_csv("data.csv")   # adjust path
   print(df.head())
   ```

---

## How to Use Hugging Face Datasets
1. Install the `datasets` library:
   ```bash
   pip install datasets
   ```
2. Load directly by dataset ID:
   ```python
   from datasets import load_dataset
   ds = load_dataset("awsaf49/persona-chat")
   print(ds["train"][0])
   ```
3. Convert to Pandas if needed:
   ```python
   df = ds["train"].to_pandas()
   ```
