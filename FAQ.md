# Frequently Asked Questions (FAQ)

## General

### What is PersonaBase?
PersonaBase is a repository of computational resources for data-driven persona (DDP) research. It provides shared datasets, generative AI prompts, example computational notebooks, persona systems, and standardized resources to enable reproducible benchmarking and collaborative scientific study across the persona research community.

### Who is PersonaBase for?
PersonaBase targets two primary audiences:

- **Novice DDP researchers** seeking guidance on how to generate and evaluate data-driven personas. PersonaBase provides practical example notebooks, ready-to-use datasets, and curated prompts so you can learn by doing—without needing to collect your own data first.
- **Experienced DDP researchers** seeking to improve the state-of-the-art. PersonaBase provides a shared foundation for benchmarking new methods against existing approaches using standardized datasets and metrics.

### What does PersonaBase contain?
PersonaBase includes:

- **computational notebooks** — for persona development (PD01a–PD05a) and persona evaluation (PE01a–PE06b)
- **datasets** with either user data or personas (both synthetic and real)
- **persona generation and evaluation prompts** collected from published research
- **persona systems** cataloged from top HCI venues
- **related repositories** with additional DDP resources

### What problem does PersonaBase solve?
DDP research currently lacks systematically developed benchmarking resources and practices. Reviews have found that less than 10% of persona studies share resources such as code, datasets, or algorithms. PersonaBase addresses this gap by aggregating and organizing computational resources specifically for DDP benchmarking, enabling reproducibility, comparison of methods, and measurable scientific progress.

---

## Getting Started

### What are the prerequisites for using PersonaBase?
To run the computational notebooks, you will need:

- **Python 3.8+** with common data science libraries (NumPy, pandas, scikit-learn, matplotlib)
- **Jupyter Notebook** or **JupyterLab** for running `.ipynb` files
- Basic familiarity with Python programming and data science concepts
- For LLM-based notebooks (e.g., PD05a): access to an LLM API (e.g., OpenAI, Anthropic)

If you have never used Python, the notebooks may not be the best starting point for you. However, the prompts (PP01–PP27), system descriptions (PS01–PS19), and dataset listings (DS01–DS12) do not require programming skills and can still be valuable.

### Where do I start?
It depends on your goal:

| Your Goal | Start Here |
|---|---|
| I want to **learn** how to create data-driven personas | Start with the persona development notebooks (PD01a–PD05a). PD02a (clustering) is a good first notebook if you are new to DDP methods. |
| I want to **evaluate** personas I have already created | Start with the persona evaluation notebooks (PE01a–PE06b). PE06b provides a unified evaluation combining fairness, diversity, coverage, and consistency. |
| I want to **generate personas using LLMs** | Browse the prompts collection (PP01–PP27) for ready-to-use prompts, or see notebook PD05a for an LLM-based persona generation workflow. |
| I want to **compare persona generation methods** | See PE05b for benchmarking segmentation techniques and PE06b for a leaderboard-style comparison of five methods. |
| I want to **find a dataset** to experiment with | Browse the datasets listing (DS01–DS12). DS01 and DS03 contain user data for persona development; others contain pre-built personas. |
| I want to **explore existing persona systems** | Browse the systems listing (PS01–PS19). Five systems have publicly available source code (PS04, PS08, PS10, PS12, PS15). |

### I have my own data. What can I do with it?
You can adapt the persona development notebooks to your data:

- **Survey or structured demographic data** → Try PD02a (clustering), PD03a (PCA), or PD04a (Gaussian mixture models)
- **Social media or behavioral analytics data** → Try PD01a (non-negative matrix factorization)
- **Qualitative data (interviews, transcripts, open-ended surveys)** → Try PD05a (LLM-based methods) or adapt prompts from the prompts collection
- **Pre-existing personas you want to evaluate** → Use the evaluation notebooks PE01a–PE06b

### I don't have any data yet. Can I still use PersonaBase?
Yes. PersonaBase includes 12 datasets you can use for experimentation and learning. The development notebooks (PD01a–PD05a) also use simulated data (indicated by the "a" suffix), so you can run them immediately without any data collection.

---

## Understanding the Taxonomy

### How are resources organized?
Resources follow a naming convention where the first two letters indicate the resource type, followed by a numerical identifier and a letter suffix:

| Prefix | Resource Type |
|---|---|
| **PD** | Persona Development (notebook) |
| **PE** | Persona Evaluation (notebook) |
| **DS** | Dataset |
| **PP** | Prompt |
| **PS** | Persona System |
| **PR** | Persona Repository |

### What do the "a" and "b" suffixes mean?
- **"a"** = the resource uses **simulated or synthetic data** (e.g., PD01a)
- **"b"** = the resource uses **real, anonymized data** (e.g., PE03b)

---

## Notebooks

### What persona development methods are covered?
The five development notebooks demonstrate:

| Notebook | Method | Description |
|---|---|---|
| PD01a | Non-Negative Matrix Factorization (NMF) | Persona generation from YouTube-like audience behavior data |
| PD02a | Clustering Analysis | Grouping users into persona segments via clustering algorithms |
| PD03a | Principal Component Analysis (PCA) | Dimensionality reduction for identifying persona dimensions |
| PD04a | Gaussian Mixture Models (GMM) | Probabilistic segmentation of user populations |
| PD05a | LLM-Based Methods | Using large language models for persona generation |

### What evaluation methods are covered?
The six evaluation notebooks demonstrate:

| Notebook | Focus | Description |
|---|---|---|
| PE01a | Persona Perception Scale | Measuring user perception of persona quality |
| PE02a | Diversity | Quantifying how diverse a persona set is |
| PE03a | Coverage | Analyzing the relationship between persona set size and dataset coverage |
| PE04a | Behavioral Metrics | Tracking interaction metrics in persona systems |
| PE05b | Segmentation Benchmarking | Comparing different segmentation techniques |
| PE06b | Unified Evaluation | Combining fairness, diversity, coverage, and consistency into a leaderboard |

### How were the notebooks created and verified?
The notebooks were generated using Claude 4-Sonnet with prompting from the lead researcher (Associate Professor with multiple years of DDP and computational experience). They underwent a two-stage verification process: (1) the lead author verified code and outputs, resolving issues through iterative prompting, and (2) a PhD researcher with industry programming experience independently validated the code. The released notebooks are functionally correct and produce the expected outputs.

### Can I modify the notebooks for my own use?
Absolutely. The notebooks are designed to be adapted. You can swap in your own datasets, adjust algorithm parameters, or extend the evaluation metrics to suit your research context.

---

## Datasets

### What types of datasets are available?
PersonaBase contains 12 datasets spanning:

- **Persona development data** (user data for creating personas) — DS01, DS03
- **Persona descriptions** (pre-built persona profiles) — 5 datasets
- **Persona dialogues** (conversational data with persona conditioning) — 4 datasets
- **Specialized datasets** (e.g., deepfake personas, bias analysis) — DS06, DS09

### Are the datasets real or synthetic?
Both. Three datasets (25%) contain real data (all published before 2023), while nine datasets (75%) are synthetic/AI-generated (all from 2023 onward). This reflects the broader trend toward LLM-generated synthetic persona data.

### Are there datasets I can use for HCI-focused research specifically?
Four datasets are HCI-focused: DS01 and DS03 (persona development from user data), DS06 (immersive deepfake personas), and DS09 (demographic and bias analysis of LLM-generated personas). The remaining eight are more oriented toward NLP/ML applications.

---

## Prompts

### How can I use the prompts?
The 27 prompts can be copied directly and adapted for your own persona generation or evaluation tasks with any LLM. They are organized into two categories:

- **Persona Generation Methods** (20 prompts, 74.1%) — for creating personas, including direct generation, demographic-driven synthesis, attribute-based generation, summary-to-detailed approaches, and iterative workflows
- **Persona Evaluation and Application** (7 prompts, 25.9%) — for evaluating, validating, or interacting with personas

### Do I need a specific LLM to use the prompts?
No. The prompts are LLM-agnostic and can be used with any large language model (e.g., GPT-4, Claude, Gemini, Llama, etc.). You may need to adjust formatting or system instructions depending on the specific model you use.

---

## Evaluation and Benchmarking

### How do I know if my personas are "good"?
PersonaBase operationalizes several quality dimensions from the literature:

- **Consistency** — Internal coherence of persona attributes
- **Diversity** — Representation of varied user segments
- **Coverage** — How well the persona set accounts for the underlying user population
- **Fairness** — Equitable representation across demographic groups

Notebook PE06b combines all four dimensions into a unified evaluation framework with a leaderboard-style comparison.

### What baselines can I compare against?
The PE05b and PE06b notebooks benchmark five persona generation methods: Spectral clustering, NMF, PCA, UMAP, and K-Means clustering. You can use these as baselines when evaluating your own methods. The 19 cataloged persona systems (PS01–PS19) can also serve as reference points.

### Is there a leaderboard?
PE06b demonstrates a leaderboard-style evaluation that ranks persona generation methods across multiple criteria (accuracy, consistency, diversity, coverage). You can extend this to include your own methods.

---

## Contributing and Community

### Can I contribute to PersonaBase?
Yes, contributions are welcome! You can contribute by:

- Submitting new datasets, prompts, or notebooks via pull requests
- Reporting issues or suggesting improvements
- Sharing your own persona systems or evaluation approaches
- Proposing new benchmarking tasks or metrics

### How can I cite PersonaBase?
If you use PersonaBase in your research, please cite:
*(Citation details will be updated upon publication.)*

### How will PersonaBase be maintained?
We plan to keep PersonaBase current by adding new datasets, notebooks, prompts, and systems as they emerge. Both persona methods and computational capabilities evolve, so the repository requires continuous maintenance. Community contributions are essential to this effort.

---

## Troubleshooting

### A notebook throws an error. What should I do?
1. Ensure you have all required Python packages installed (check the import statements at the top of each notebook).
2. Verify you are using Python 3.8 or later.
3. Check that any referenced data files are in the correct directory.
4. If the issue persists, please open a GitHub issue with the error message and your environment details.

### The datasets are too large / too small for my use case. What should I do?
- **Too large**: Most notebooks can work with subsampled data. You can use pandas `.sample()` to reduce dataset size.
- **Too small**: Consider using LLMs to generate synthetic data that supplements your existing data (see PD05a for an example workflow), or combine multiple datasets.

### I come from a qualitative research background. Is PersonaBase relevant for me?
PersonaBase is primarily designed for computational DDP research and does require some programming skills for the notebooks. However, the following resources do not require coding and may still be valuable:

- The **prompts collection** (PP01–PP27) can be used directly with any LLM chatbot interface
- The **systems catalog** (PS01–PS19) provides an overview of existing DDP tools
- The **datasets listing** (DS01–DS12) can help you understand what data is available

If you are interested in transitioning from qualitative to quantitative persona methods, the development notebooks (PD01a–PD05a) with their simulated data provide a structured, hands-on learning path.

---

## Contact

For questions, suggestions, or collaboration inquiries, please open a GitHub issue or contact the maintainers directly.
