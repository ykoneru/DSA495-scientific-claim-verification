# DSA495-scientific-claim-verification

> **DSA 495 Topic Brief**
>
> Replace the bracketed prompts below with your team’s information. Keep this file at the root of your team’s project repository and name it `README.md`.

## Before You Begin

- Create **one shared project repository per team** and continue using it through the end of the semester. Do not create separate repositories for the Topic Brief and later stages of the project.
- The repository name must begin with the case-sensitive prefix **`DSA495`**, such as `DSA495-news-classification`. After the prefix, feel free to choose a creative and distinctive team name; it does not have to describe your task or topic. A repository whose name does not begin with `DSA495` will receive zero credit for the Topic Brief.
- Complete every required section and item below. Anything labeled optional may be left undecided! If another required item does not apply, write “Not applicable” and briefly explain why. Feel free to add sections as needed, but keep the brief concise.
- Make sure the repository is accessible to the instructor by choosing one of the following options:
  1. **Public repository:** No collaborator invitation is required.
  2. **Private repository:** Add the instructor as a collaborator using the GitHub username `SerenaYKim`.
- Do not upload sensitive or restricted information to GitHub, even in a private repository. If your project uses such data, keep it in a shared team drive and use GitHub for code, documentation, and other materials that can be shared safely.

## Team Members

- Yogya Koneru

## One-Sentence Task

**Given a scientific claim, we will retrieve and compare research papers relative to the claim and compare the evidence to see if it supports or contradicts the specific claim.**

## Illustrative Input and Desired Output

- **Example input:** Getting enough sleep improves concentration and focus throughout the day.
- **Desired output:** I would get a list of different studies about sleep ranked from most important to least important in regards to the claim, and then the program would show any evidence that supports or contradicts the claim.

## Background and Starting Point

We see a lot of scientific claims online, but it can be difficult to know if there is actual research supporting them. There are so many studies available that finding the right one can take a lot of time. Even after finding a study, we still have to read through it to understand what the researchers found and whether it agrees with the claim. I became interested in this project because I thought it would be useful to have a program that makes finding this information easier.

## Intended Output and Success

I want to make a Python program where someone can enter a scientific claim and get back a list of research papers that are related to it. The program would rank the results and show the titles or IDs of the studies. Since the SciFact dataset includes labels for some of the evidence, I also want to show the sentences that researchers marked as supporting or contradicting the claim. I think this could help students and researchers who want to find studies about something they have read or heard. The program would help people find evidence, but it would not automatically mean that a claim is true or false.

**Success statement:** I would consider the project successful if it can find studies that contain useful evidence and rank them near the top, so people do not have to spend as much time looking for them.

## Preferred Data

### Corpus

I plan to use SciFact, which has around 5,183 research paper summaries and 1,400 scientific claims. Each summary counts as one document. The dataset includes paper titles, text, IDs, and labels showing which sentences support or contradict a claim. The main files are corpus.jsonl for the papers and claims_train.jsonl and claims_dev.jsonl for the labeled claims.

### Source and Access

- **Dataset or corpus name:** SciFact
- **Original source organization or creator:** Researchers from the Allen Institute for AI and their collaborators.
- **Original collection process:** Researchers made claims from scientific papers and labeled evidence as supporting or contradicting them. The paper summaries came from the Semantic Scholar Open Research Corpus (S2ORC).
- **Direct link:** https://github.com/allenai/scifact
- **Access method:** Download the JSONL files using the instructions on GitHub.
- **Access, licensing, privacy, or redistribution considerations:** The claims and labels use CC BY 4.0, while the paper summaries use ODC-By 1.0. I would credit the original researchers and link to the data instead of uploading it again. I would also make it clear that the results are not medical advice.
- **Backup corpus (optional):** If SciFact doesn't work out, I could use a smaller public set I can find on the internet.

### Examples

Scientific claim: “Antiretroviral therapy increases rates of tuberculosis across a broad range of CD4 strata.” The dataset has evidence in document 4883040 that contradicts this claim.

Scientific claim: “Citrullinated proteins externalized in neutrophil extracellular traps act indirectly to disrupt the inflammatory cycle.” The dataset showscontradicting evidence in documents 11328820 and 30041340

### Fit with the Task

I think SciFact is a good choice because it has both the research papers I want to search through and labels showing which ones contain evidence for different claims. This means I can compare the papers my program finds with the ones that researchers have already marked as relevant. One limitation is that the dataset only includes short summaries of papers rather than the full studies. This means some important information might be missing. Also, a paper that is not marked as evidence could still contain useful information, so I would need to keep that in mind when looking at my results.

## Feasibility and Immediate Next Steps

- **Minimum viable project:** I want to build a Python program that finds the five most relevant research paper summaries for a scientific claim. I will use sentence embeddings and cosine similarity to find papers that are related to the claim.
- **Data-access check:** I have looked through the SciFact GitHub page but have not downloaded the data yet. My next step is to download it and make sure I can read the files.
- **Largest current risk:** The program might find papers about the same topic that do not actually contain evidence supporting or contradicting the claim.
- **Backup plan:** If predicting whether evidence supports or contradicts a claim becomes too difficult, I will focus on only finding relevant papers and use the already known SciFact labels to check my results.
- **Next two actions:**
  1. Download SciFact and look over its claims and paper summaries — Yogya Koneru — October 22, 2026.
  2. Build and test a search program using sentence embeddings and cosine similarity — Yogya Koneru — October 25, 2026.

## Possible Text-Analysis Method and Evaluation (Optional)

I plan to use sentence embeddings and cosine similarity to find research papers that are related to a scientific claim. I will use Python to compare the results with the existing labels in SciFact to see how often the program finds the correct papers. I also want to look at cases where the program makes mistakes to understand what could be improved. If I have enough time, I would like to use text classification to predict whether evidence supports or contradicts a claim.

## Questions for the Instructor

- [What feedback would help your team move forward? You might ask about scope, data feasibility, methods, evaluation, tools, or project risks.]
- [Add another question, or write “No additional questions at this time.”]

## AI-Use Statement

[Identify any generative or agentic AI tool used to prepare this brief, its purpose, the work completed before consulting it, the advice incorporated, and how the output was verified. If your team did not use such a tool, state that clearly.]
