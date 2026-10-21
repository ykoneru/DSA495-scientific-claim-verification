# DSA495-scientific-claim-verification

## Team Members

- Yogya Koneru

## One-Sentence Task

**Given a scientific claim, we will find and rank research paper summaries based on how closely they relate to the claim and show any available evidence that supports or contradicts it.**

## Illustrative Input and Desired Output

- **Example input:** "Vitamin D supplementation reduces the risk of respiratory infections."
- **Desired output:** A list of the five most relevant research paper summaries, ranked by how closely they relate to the claim. The program would show each paper's title, ID, and similarity score, along with relevant sentences from the summaries. For claims already in SciFact, it could also show any available evidence labels.

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
- **Data-access check:** I downloaded the SciFact dataset and used Python to open the three main files: corpus.jsonl, claims_train.jsonl, and claims_dev.jsonl. I looked through the files to make sure they had the research paper summaries, claims, and evidence labels.
- **Largest current risk:** The program might find papers about the same topic that do not actually contain evidence supporting or contradicting the claim.
- **Backup plan:** If predicting whether evidence supports or contradicts a claim becomes too difficult, I will focus on only finding relevant papers and use the already known SciFact labels to check my results.
- **Next two actions:**
  1. Look through some of the claims, paper summaries, and evidence labels to better understand how the dataset works — Yogya Koneru — October 22, 2026.
  2. Make a basic program using sentence embeddings and cosine similarity to find research papers related to a claim — Yogya Koneru — October 25, 2026.

## Possible Text-Analysis Method and Evaluation (Optional)

I plan to use sentence embeddings and cosine similarity to find research papers that are related to a scientific claim. I will use Python to compare the results with the existing labels in SciFact to see how often the program finds the correct papers. I also want to look at cases where the program makes mistakes to understand what could be improved. If I have enough time, I would like to use text classification to predict whether evidence supports or contradicts a claim.

## Questions for the Instructor

Would focusing on finding and ranking the research papers be enough for the final project if I cannot finish predicting whether evidence supports or contradicts a claim?

## AI-Use Statement

After coming up with interests I have on my own, I used AI tools to help brainstorm project ideas by giving it my resume and asking for interesting projects I could make to enhance my resume. I also used it to, after manually checking, verify the quality of different datasets for my project. I selected a project that was at the intersection of my own interests, and after from AI suggestions, which is how I landed on this idea. 
