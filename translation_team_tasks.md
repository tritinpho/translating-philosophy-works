# Translation Team Preparation Tasks
*For LLM + RAG Philosophy Translation Pipeline*

---

## 1. 🖋️ Writing Style Analysis (from your preferred writer)

The goal is to give the AI enough signal to **imitate the tone, rhythm, and voice** of your chosen writer.

### Tasks
- **Collect a writing corpus**: Gather 20–50 representative excerpts from the writer's work — varying in topic, length, and formality. Longer is better (aim for 30,000+ words total).
- **Annotate stylistic traits**: For each excerpt, note:
  - Sentence length tendency (short & punchy vs. long & layered)
  - Use of rhetorical devices (questions, repetition, parallelism)
  - Level of formality and register
  - Preferred paragraph structure
  - Typical transition phrases (e.g., *"Nói cách khác…"*, *"Hơn thế nữa…"*)
- **Create a Style Guide document**: Summarize the writer's voice in 1–2 pages. Include:
  - "This writer DOES: …"
  - "This writer AVOIDS: …"
  - 5–10 before/after examples showing style transformation

---

## 2. 📖 Philosophy Glossary Unification

Philosophical terminology must be **consistent across all translations**. Inconsistency is the #1 quality problem in philosophy translation.

### Tasks
- **Draft a master glossary** (spreadsheet with columns):
  - English term | Vietnamese translation | Notes / context | Source authority | Disputed? (Y/N)
- **Prioritize high-frequency terms first**: metaphysics, epistemology, ethics, logic, phenomenology
- **Research existing Vietnamese standards**: Check how established Vietnamese philosophy academics/translators have rendered key terms (e.g., textbooks from ĐHKHXH&NV, Hanoi National University)
- **Flag disputed terms**: Some terms have multiple competing translations — document all options and pick one authoritatively
- **Add example sentences**: For each term, include one example sentence in context (both EN and VI)
- **Categorize by domain**: Aristotle terms, Kantian terms, existentialist terms, etc.
- **Review and vote**: Have the whole team agree on final choices before locking the glossary

> [!IMPORTANT]
> The glossary will be injected directly into the AI's system prompt. Keep definitions concise and unambiguous.

---

## 3. 📚 Parallel Corpus Building (for RAG retrieval)

RAG works by retrieving **relevant reference passages** to show the AI as examples. You need a library of high-quality EN↔VI translation pairs.

### Tasks
- **Source existing bilingual philosophy texts**:
  - Officially published Vietnamese translations of philosophy works
  - Academic theses with bilingual abstracts
  - Bilingual journals (e.g., *Tạp chí Triết học*)
- **Format each pair as a document chunk**: One English paragraph + its Vietnamese translation. Split at natural paragraph boundaries, not mid-sentence.
- **Tag each chunk with metadata**:
  - Author | Work title | Domain (ethics, metaphysics, etc.) | Difficulty level | Translation quality (1–3 stars)
- **Mark chunks that exemplify the target writing style**: These are priority retrieval candidates — flag them clearly.
- **Minimum target**: 500–1,000 high-quality paragraph pairs before launch

---

## 4. 📝 System Prompt & Instructions Drafting

Someone (non-technical) needs to write the **natural language instructions** that will guide the AI.

### Tasks
- **Write the base system prompt** covering:
  - Role definition ("You are a philosophy translator specializing in...")
  - Tone & style instructions (reference the Style Guide)
  - Rules for handling untranslatable terms
  - Rules for footnoting or annotating difficult concepts
  - Sentence structure preferences
- **Draft edge-case instructions**:
  - What to do when a term is in the glossary (always use it)
  - What to do when a term is NOT in the glossary (transliterate + note)
  - How to handle quotes within quotes
  - How to handle gendered language (English has less, Vietnamese has more)
- **Test the instructions by hand**: Read the prompt yourself and ask "would a human translator understand these rules clearly?"

---

## 5. 🔍 Quality Assurance (QA) Rubric

Your team will review AI output. They need a **clear rubric** to evaluate consistently.

### Tasks
- **Define quality dimensions** (score 1–5 each):
  | Dimension | What to check |
  |-----------|--------------|
  | Accuracy | Is the meaning faithfully preserved? |
  | Terminology | Are glossary terms used correctly? |
  | Style match | Does it sound like the target writer? |
  | Fluency | Is the Vietnamese natural and readable? |
  | Footnotes | Are difficult concepts appropriately noted? |
- **Create sample "gold standard" translations**: 10–20 paragraphs translated by your best human translator. These become benchmarks.
- **Write a reviewer checklist** (1 page): A quick pass/fail checklist each reviewer uses before approving output.

---

## 6. 🗂️ Workflow & Process Documentation

### Tasks
- **Define the translation pipeline** (who does what):
  ```
  Source text → AI draft → Reviewer edits → Senior editor approves → Published
  ```
- **Create a feedback loop**: Reviewers should log every correction they make, with the category of error. This data improves future prompts and the glossary.
- **Version control the glossary**: Every time a term changes, log who changed it, when, and why.
- **Establish style arbitration**: Who has the final vote when the team disagrees on a translation choice?

---

## 📅 Suggested Priority Order

| Priority | Task | Owner |
|----------|------|-------|
| 🔴 First | Master glossary (top 200 terms) | Senior translator(s) |
| 🔴 First | Style guide from writer corpus | Editor |
| 🟠 Second | Parallel corpus (500+ pairs) | Full team |
| 🟠 Second | System prompt draft | Editor + project lead |
| 🟡 Third | QA rubric + gold standards | Senior translator(s) |
| 🟡 Third | Workflow documentation | Project lead |
