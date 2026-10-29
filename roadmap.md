[roadmap.md](https://github.com/user-attachments/files/34136181/roadmap.md)
# 12-Week Roadmap: From Clinician to AI Safety Practitioner

A learning plan for a doctor with no coding background to reach an intermediate level in AI safety and evals, with a focus on medical AI. It ends with a capstone: a medical safety evaluation of a language model.

**Time budget:** 2 hours per day, Monday to Friday (about 10 hours a week, about 120 hours in total). Saturday and Sunday are rest days.

## How each week works

| Day | Focus |
|---|---|
| Mon | Learn: main course or reading for the week |
| Tue | Learn: continue, take notes |
| Wed | Practice: exercises or hands-on work |
| Thu | Practice: apply it to a medical example |
| Fri | Build: add something to this repo (notes, resource entries, flashcards), then commit |

Every week has a **Done when** checkpoint. If you have not met it, spend the next week's first day finishing it rather than moving on.

## Tools (no installation needed)

- **GitHub in the browser:** create and edit files with the web editor and the green "Commit changes" button. You do not need the command line at any point in this plan.
- **Google Colab:** run Python in the browser for free.

---

## Phase 1: Foundations (Weeks 1-3)

### Week 1: Setup and Python basics
- Learn GitHub's web interface: create a repository, add a file, edit it, commit.
- Start a beginner Python course (suggestions: CS50's Introduction to Programming with Python, or Automate the Boring Stuff with Python).
- Cover: variables, strings, numbers, input and output, if statements.
- Add this roadmap to your repo as `roadmap.md` and write a short README.

**Done when:** your repo is public, it has a README and this roadmap, and you have run 10 small Python programs in Colab.

### Week 2: Python continued
- Cover: loops, functions, lists, dictionaries, reading and writing files, JSON.
- Practice with medical data: a list of lab values, a dictionary of drug doses, a loop that flags abnormal results.
- Create the `/resources` folder and add your first 5 annotated entries (title, link, what it covers, your verdict).

**Done when:** you can write a function from scratch and loop over a list of dictionaries.

### Week 3: Machine learning fundamentals
- Learn what machine learning is, supervised vs unsupervised learning, training vs test data, overfitting.
- Learn evaluation metrics through clinical language: sensitivity, specificity, precision, recall, accuracy, and why accuracy can mislead on rare diseases.
- Suggested sources: Google's Machine Learning Crash Course, or fast.ai's practical deep learning course (first lessons).
- Create `/study-materials` and write your first 20 flashcards.

**Done when:** you can explain overfitting and the sensitivity/specificity trade-off to another doctor in plain words.

---

## Phase 2: How models work and what can go wrong (Weeks 4-6)

### Week 4: Neural networks and language models
- Watch 3Blue1Brown's neural network series and Andrej Karpathy's "Intro to Large Language Models" talk.
- Learn: neurons and layers, training, tokens, what a language model actually predicts, why it can sound confident and be wrong.
- Write a one-page explainer in your own words: "How an LLM works, for clinicians" (this seeds your tutorial).

**Done when:** you can explain what a token is, what training does, and why hallucination happens.

### Week 5: AI safety foundations
- Take or follow the BlueDot Impact AI Safety Fundamentals curriculum (or its public readings).
- Learn: the alignment problem, specification gaming and reward hacking, misuse vs accidental harm, why capability and safety are different things.
- Read "Concrete Problems in AI Safety" (the introduction and one section).

**Done when:** you can define alignment, give two real examples of specification gaming, and explain the difference between misuse and accident risks.

### Week 6: Interpretability, robustness, and medical AI risks
- Learn what interpretability research is trying to do (a gentle introduction, such as Neel Nanda's or Anthropic's accessible overviews).
- Learn robustness and distribution shift.
- Medical AI risks: bias across populations, hallucinated clinical facts, automation bias, a model trained in one hospital failing in another (very relevant to African health settings).
- Skim how regulators think about this (FDA guidance on AI-enabled devices, WHO guidance on AI for health).

**Done when:** you have a written list of 8 ways a clinical AI tool can fail, each with a one-line real-world example.

---

## Phase 3: Evals and red-teaming (Weeks 7-9)

### Week 7: What an eval is
- Learn: benchmarks vs custom evals, test sets, scoring methods, rubrics, LLM-as-judge, contamination and benchmark saturation.
- Study existing medical evals: MedQA, HealthBench, MedHELM. What do they measure, and what do they miss?
- Suggested reading: documentation and papers for those benchmarks, and the UK AI Security Institute's Inspect evaluation framework docs.

**Done when:** you can describe three existing medical benchmarks and one weakness of each.

### Week 8: Run your first eval
- In Colab, write a small Python script that sends 10 medical questions to a model through an API, collects the answers, and scores them against an answer key.
- Note: API use may cost a small amount; use free tiers or a small credit and keep the test small.
- Save the notebook to `/capstone/practice`.

**Done when:** you have a notebook that runs end to end and produces a score table.

### Week 9: Red-teaming and safety evals
- Learn: adversarial prompting, sycophancy (a model agreeing with a wrong claim), refusal behaviour, over-refusal, escalation of harm.
- Draft a taxonomy of medical safety failures for your capstone, for example: dangerous dosing advice, missed red-flag symptoms, false reassurance, agreeing with a patient's incorrect belief, failing to recommend urgent care.

**Done when:** you have a taxonomy with at least 6 categories and 3 example prompts for each.

---

## Phase 4: Capstone and tutorial (Weeks 10-12)

### Week 10: Design the capstone eval
- Write about 30 clinical safety scenarios from your taxonomy. This is where your medical training is the advantage.
- Write a scoring rubric (for example: safe, partially safe, unsafe) with clear criteria, so another clinician would score the same way.
- Ask one or two doctor friends to review a sample of the scenarios and the rubric.

**Done when:** `/capstone` contains the scenarios and the rubric, reviewed by at least one other clinician.

### Week 11: Run and analyse
- Run the scenarios on one or two models. Score the responses with your rubric.
- Do an error analysis: which categories fail most, and why? Include 3 to 5 example failures with your commentary.
- Make a simple chart of results by category.

**Done when:** you have a results table, a chart, and written findings.

### Week 12: Write-up and publish
- Write the capstone report (1,000 to 1,500 words): question, method, results, limitations, what you would do next.
- Turn your notes into the final `/guide`: "How to evaluate a medical AI model, written for clinicians."
- Polish the README so a stranger understands the project in 60 seconds.
- Share it on LinkedIn and send it to people in digital health and medical AI.

**Done when:** the repo is public and polished, and you have posted about it.

---

## Final repository structure

```
/README.md
/roadmap.md
/resources        annotated library (30-40 entries)
/study-materials  flashcards and quizzes
/guide            the clinician's tutorial on evaluating medical AI
/capstone         scenarios, rubric, code, results, write-up
```

## Notes

- Resource names above are starting points. Check that each is still current and free before you rely on it, and replace any that have changed.
- Add to `/resources` every week, not only in the weeks that mention it.
- If you fall behind, shrink the scope of the capstone rather than skipping the earlier weeks.
