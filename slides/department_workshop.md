---
marp: true
theme: default
size: 16:9
paginate: true
header: 'ODISSEI SoDa · LLM-based data annotation'
footer: 'ODISSEI SoDa Workshop · LLM-based data annotation'
style: |
  section {
    background: #ffffff;
    color: #595959;
    font-family: 'Aptos', 'Arial', sans-serif;
    font-size: 29px;
    line-height: 1.23;
    padding: 68px 72px;
  }
  section h1 { color: #006889; font-size: 1.5em; }
  section h2 { color: #006889; font-size: 1.15em; }
  section h3 { color: #006889; }
  section a { color: #006889; }
  section header, section footer, section::after { color: #808080; }
  section table th { background: #f2f5f6; color: #006889; }
  section table tr { background: #ffffff; }
  section table tr:nth-child(2n) { background: #f7f7f7; }
  section strong { color: #006889; }
  section ul, section ol { margin-top: 0.35em; }
  section li { margin: 0.18em 0; }
  section code { font-size: 0.84em; }
  section pre { background: #f2f5f6; padding: 16px 22px; border-radius: 8px; }
  section blockquote { border-left: 5px solid #006889; background: #f2f5f6; padding: 0.3em 0.8em; }
  section.title { background: #ffffff; color: #808080; }
  section.title h1, section.title strong { color: #006889; }
  section.title h2 { color: #808080; }
  section.title header, section.title footer { color: #808080; }
  section.exercise { background: #ffffff; }
  section.exercise h1, section.exercise h2 { color: #006889; }
  section.checkpoint { background: #ffffff; }
  section.checkpoint h1, section.checkpoint h2 { color: #006889; }
  section.optional { background: #ffffff; }
  section.optional h1, section.optional h2 { color: #006889; }
  section.small { font-size: 25px; }
  section header { padding-right: 180px; }
  section header::after {
    content: '';
    position: fixed;
    top: 12px;
    right: 32px;
    width: 150px;
    height: 52px;
    padding: 4px 8px;
    background: url('img/soda.png') center / contain no-repeat;
    background-origin: content-box;
    border-radius: 4px;
  }
  section.cover header::after { display: none; }
  section.cover { justify-content: flex-start; padding: 88px 96px; }
  section.cover header, section.cover footer, section.cover::after { display: none; }
  section.cover .cover-logo { display: block; width: 260px; height: auto; }
  section.cover .cover-brand { margin: 0 0 36px -28px; }
  section.cover h1 { font-size: 58px; line-height: 1.12; margin: 0 0 20px; letter-spacing: -1px; }
  section.cover h2 { font-size: 34px; font-weight: 600; margin: 0; }
  section.cover .cover-details { margin-top: 68px; font-size: 23px; line-height: 1.5; color: #808080; }

  section.cover .cover-materials { position: absolute; right: 96px; bottom: 100px; width: 220px; text-align: center; }
  section.cover .cover-materials p { margin: 0 0 10px; font-size: 23px; font-weight: 600; color: #006889; }
  section.cover .cover-materials img { display: block; width: 220px; height: auto; }

  section.fellowship .fellowship-layout { display: grid; grid-template-columns: 1fr 265px; gap: 36px; align-items: start; }
  section.fellowship ul { font-size: 27px; line-height: 1.3; }
  section.fellowship li { margin: 0.45em 0; }
  section.fellowship .fellowship-deadline { margin-top: 20px; padding: 24px 18px; background: #006889; color: #ffffff; text-align: center; font-size: 27px; line-height: 1.3; }
  section.fellowship .fellowship-deadline strong { color: #ffffff; font-size: 32px; }

  section.revision-files .file-comparison { display: grid; grid-template-columns: 1fr 1fr; gap: 54px; }
  section.revision-files h2 { margin: 0 0 14px; font-size: 31px; }
  section.revision-files pre { margin: 0; font-size: 23px; line-height: 1.3; background: none; padding: 0; }
  section.revision-files .saved-history { margin-top: 16px; font-size: 23px; line-height: 1.35; }
  section.revision-files .saved-history p { margin: 0 0 6px; }
  section.revision-files .comparison-caption { margin-top: 26px; font-size: 25px; }

  section .qr-center { display: flex; justify-content: center; width: 100%; }
  section .qr-center img { width: 300px; height: auto; }
  section.mission { text-align: center; }
  section.mission h1 { color: #404040; font-size: 48px; line-height: 1.18; }
  section.mission p { color: #808080; font-size: 29px; max-width: 1000px; margin: 24px auto 0; }
  section.team .team-layout { display: grid; grid-template-columns: 1.15fr 1fr; gap: 42px; align-items: center; }
  section.team .team-copy { font-size: 23px; line-height: 1.25; }
  section.team .team-copy h2 { color: #404040; font-size: 26px; margin: 15px 0 5px; }
  section.team .team-copy p { margin: 0; }
  section.team .team-photo { width: 100%; height: auto; }
  section.foundation .foundation-core { margin-top: 18px; padding: 18px 24px; border-radius: 12px; background: #e3eff3; text-align: center; }
  section.foundation .foundation-core h2 { margin: 0; font-size: 34px; }
  section.foundation .foundation-core p { margin: 4px 0 0; }
  section.foundation .foundation-core .foundation-subtitle { color: #404040; font-size: 26px; }
  section.foundation .foundation-details { font-size: 21px; color: #808080; }
  section.foundation .foundation-link { margin: 10px 0; text-align: center; font-size: 21px; color: #808080; }
  section.foundation .foundation-link span { display: block; font-size: 28px; line-height: 1; color: #006889; }
  section.foundation .foundation-clients { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
  section.foundation .foundation-client { display: grid; grid-template-columns: 64px 1fr; align-items: center; gap: 18px; padding: 14px 20px; border: 2px solid #d9e3e6; border-radius: 12px; }
  section.foundation .foundation-client h2 { margin: 0; color: #404040; font-size: 28px; }
  section.foundation .foundation-client p { margin: 4px 0 0; }
  section.foundation .foundation-logo { width: 64px; height: 64px; }
  section.foundation .foundation-others { margin-top: 10px; text-align: center; font-size: 21px; color: #808080; }
  section.foundation .foundation-summary { margin-top: 20px; padding-top: 14px; border-top: 2px solid #d9e3e6; text-align: center; font-size: 25px; color: #404040; }
  section.change-steps .change-zones { display: grid; grid-template-columns: 2fr 1fr; gap: 16px; margin-top: 18px; }
  section.change-steps .change-zone { padding: 14px 18px 18px; border-radius: 14px; background: #f2f5f6; }
  section.change-steps .change-zone.remote { background: #e3eff3; }
  section.change-steps .change-zone-title { margin-bottom: 10px; font-size: 20px; font-weight: 700; letter-spacing: 1px; text-transform: uppercase; color: #808080; }
  section.change-steps .change-cards { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
  section.change-steps .change-zone.remote .change-cards { grid-template-columns: 1fr; }
  section.change-steps .change-card { padding: 14px 16px; border: 2px solid #d9e3e6; border-radius: 10px; background: #ffffff; }
  section.change-steps .change-card h2 { margin: 0; font-size: 28px; }
  section.change-steps .change-card h2 small { font-size: 22px; font-weight: 400; color: #808080; }
  section.change-steps .change-card p { margin: 4px 0 0; font-size: 21px; }
  section.change-steps .change-pull { margin-top: 14px; padding: 12px 18px; border: 2px dashed #006889; border-radius: 10px; text-align: center; font-size: 23px; }
  section.workflow-full { padding: 26px 40px 34px; }
  section.workflow-full h1 { margin: 0 0 4px; font-size: 1.2em; }
  section.workflow-full p:has(> img:only-child) { margin: 0; text-align: center; }
  section.workflow-full p:has(> img:only-child) img { width: 100%; max-height: 585px; object-fit: contain; }
  section.workflow-full p:not(:has(img)) { margin: 6px 0 0; text-align: center; }

  section .source { font-size: 17px; color: #808080; margin-top: 18px; }
  section .lead { font-size: 32px; line-height: 1.25; }
  section .statement { font-size: 33px; color: #006889; }
  section .two { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; align-items: start; }
  section.workflow table { font-size: 24px; }
  section.workflow td:first-child { color: #006889; font-weight: 700; }
  section.screenshot { padding: 0; background: #fff; }
  section.screenshot header, section.screenshot footer, section.screenshot::after { display: none; }
  section.screenshot .screenshot-image {
    position: absolute; inset: 0; width: 100%; height: 100%;
    max-width: none; max-height: none; object-fit: contain;
    background: #fff; z-index: 100;
  }

---
<!-- _class: title cover -->
<div class="cover-brand"><img class="cover-logo" src="img/soda.png" alt="SoDa logo"></div>

# LLM-based data annotation
## Research workflows and FAIRR-LLM

<div class="cover-details">
Qixiang Fang<br>
Methodology, Statistics, and Data Science<br>
09.11.2026
</div>

---
<!-- _class: mission -->
# We help social scientists with data-intensive & computational research

Our goal is to enhance the evidence base and impact of social science by bringing the added value of new data sources and new data analysis techniques into social research in the Netherlands.

---
<!-- _class: team -->
# Who we are

<div class="team-layout">
<div class="team-copy">
<h2>Core team</h2>
<p>Computer and data scientists at postdoc or assistant professor level, with a social sciences background.</p>
<h2>Fellows</h2>
<p>Early career social scientists working on projects aligned with ODISSEI and SoDa’s mission.</p>
<h2>Student and research assistants</h2>
<p>Support SoDa projects and activities.</p>
<h2>Associate members</h2>
<p>Liaisons, including research software engineers from eScience, SCP etc.</p>
</div>
<img class="team-photo" src="img/soda-team.jpg" alt="SoDa team group photograph">
</div>

---
<!-- _class: fellowship -->
# Fellowship programme

<div class="fellowship-layout">
<div>

- **2–3 fellows per year**
- For PhD researchers, postdocs and assistant professors
- Propose your own social science research project
- **3–6 months full-time, with salary paid**
- Join the **SoDa team** at Utrecht University’s Methodology & Statistics department
- Receive mentoring from a senior team member

</div>
<div class="fellowship-deadline">
Next application deadline:<br>
<strong>7 December</strong>
</div>
</div>


---
# Measuring self-regulated learning

**Gabrielle Martins van Jaarsveld's SoDa fellowship project**

Students discuss their weekly learning goals with a rule-based chatbot.

<br>

> “I would like to catch up on my geography reading”

<br>

LLMs score goal characteristics using a carefully designed rubric (0–2).
The resulting variables support analyses of learning and study outcomes in a downstream multilevel model. 

---
# Insights from Gabrielle's SoDa fellowship

LLM-based annotations can be extremely useful, but:

1. no standard workflow
2. low reproducibility
3. overfitting
4. annotation error can bias downstream inference
5. overwhelming choices etc.

---
# Forthcoming in *Patterns*

> Fang, Q., van Kesteren, E.-J., & Garcia-Bernardo, J. (2026). A Methodological Guide to Reproducible Text Annotation with LLMs in SSH research. 

- LLMs as **measurement instruments** in empirical research
- Annotation error and downstream statistical inference
- Reproducible workflows, with Python and R examples
- **Explore, Select, Evaluate** for unbiased workflow development and assessment

---
# A workflow

includes prompt, model, settings, and data split etc.

**A workflow can overfit while the model weights stay fixed.**

---
<!-- _class: workflow -->
# Explore, Select, Evaluate

| Stage | Data role | Workflow decisions |
|---|---|---|
| Explore | Development cases | Inspect errors and revise candidates |
| Select | Separate comparison cases | Compare fixed candidates; choose and freeze one |
| Evaluate | Untouched assessment cases | Estimate the frozen workflow's performance |

---
# FAIRR-LLM

**Putting the paper's workflow into research practice**

- **Standardised annotation:** shared structure for data, prompts, and experiments
- **Protection against overfitting:** explicit splits, frozen workflows, and controlled evaluation
- **Reproducibility:** recorded prompt versions, model settings, and outputs
- **FAIR and open science:** an exportable code repository with data, metadata, and runnable Python

No programming required.

---
<!-- _class: screenshot -->
# The built-in tutorial

<img class="screenshot-image" src="assets/department_workshop/tutorial.png" alt="The built-in tutorial">

---
<!-- _class: screenshot -->
# Load the dataset and specify the reference-label column

<img class="screenshot-image" src="assets/department_workshop/dataset-labels.png" alt="Load the dataset and specify the reference-label column">

---
<!-- _class: screenshot -->
# Design and save a versioned prompt

<img class="screenshot-image" src="assets/department_workshop/prompt.png" alt="Design and save a versioned prompt">

---
<!-- _class: screenshot -->
# Split the labelled data and freeze the split

<img class="screenshot-image" src="assets/department_workshop/freeze-split.png" alt="Split the labelled data and freeze the split">

---
<!-- _class: screenshot -->
# Provide an API key

<img class="screenshot-image" src="assets/department_workshop/api-key.png" alt="Provide an API key">

---
<!-- _class: screenshot -->
# Set up a model and define a workflow

<img class="screenshot-image" src="assets/department_workshop/define-workflow.png" alt="Set up a model and define a workflow">

---
<!-- _class: screenshot -->
# Compare multiple workflows on Explore cases

<img class="screenshot-image" src="assets/department_workshop/compare-workflows.png" alt="Compare multiple workflows on Explore cases">

---
<!-- _class: screenshot -->
# Choose a workflow for final evaluation

<img class="screenshot-image" src="assets/department_workshop/choose-workflow.png" alt="Choose a workflow for final evaluation">

---
<!-- _class: screenshot -->
# Evaluate the chosen workflow on unseen cases

<img class="screenshot-image" src="assets/department_workshop/unseen-evaluation.png" alt="Evaluate the chosen workflow on unseen cases">

---
<!-- _class: screenshot -->
# Final evaluation: no way back

<img class="screenshot-image" src="assets/department_workshop/confirm-evaluation.png" alt="Final evaluation: no way back">

---
<!-- _class: screenshot -->
# Report held-out evaluation statistics

<img class="screenshot-image" src="assets/department_workshop/report-statistics.png" alt="Report held-out evaluation statistics">

---
<!-- _class: screenshot -->
# Annotate unlabelled data with the evaluated workflow

<img class="screenshot-image" src="assets/department_workshop/annotate.png" alt="Annotate unlabelled data with the evaluated workflow">

---
<!-- _class: screenshot -->
# Export everything into a reproducible folder

<img class="screenshot-image" src="assets/department_workshop/reproducible-export.png" alt="Export everything into a reproducible folder">


---
<!-- _class: small -->
# Try FAIRR-LLM: https://fairr-llm.odissei-soda.nl/
> We would love to get your feedback!

- Use **Chrome or Edge** and choose a working folder.
- Use your API key, or ask us for a **workshop key**.
- Open the default **UK parliamentary sentiment** example.
- Labels: positive, neutral, negative.

---
# A sentiment prompt

**Reusable instructions**

> Classify the sentiment of a sentence from a UK parliamentary debate as positive, neutral, or negative. Return one label only.

**Input template**

```text
Sentence: {{sentence}}
```

---
# Feedback and discussion
Where did you get stuck? 
What can be improved?
What features are missing?

