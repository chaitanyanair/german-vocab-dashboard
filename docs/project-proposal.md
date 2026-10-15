# Project Proposal: Most Common German Words, a Vocabulary Dashboard for Learners (A2 to B1)

**Author:** Chaitanya Nair
**Status:** Draft v0.1 (15 October 2026)
**Repository:** german-vocab-dashboard

---

## 1. Background and problem

Language learners are often told to study the most frequently used words first. Frequency lists exist, but they are usually long, flat tables that are hard to explore. They also don't show how much of everyday language a learner actually understands as their vocabulary grows.

This project turns open frequency data into an interactive dashboard that helps a learner decide what to study next.

## 2. Objective

Build a simple, interactive dashboard that shows:

- which German words matter most for everyday language,
- how much text a learner understands at each vocabulary size,
- which words to learn next to reach B1.

## 3. Target user

A German learner at A2 level aiming for B1. The first user is the project author, who also uses the output in daily study.

## 4. Questions the dashboard answers

- How many words does a learner need to understand a large share of everyday German?
- Which words are the most frequent, and how are they split by part of speech (nouns, verbs, adjectives)?
- Which words belong to A2 and which to B1?
- For nouns, what are the gender (der/die/das) patterns?
- Which are the next 50 most useful words I don't know yet?

## 5. Data sources

| Source | Content | Licence |
|---|---|---|
| wordhoard | German lemmas with part of speech, frequency rank, noun gender and an estimated CEFR level | CC-BY-SA-4.0 |
| Subtitle-based frequency list (e.g. the Wiktionary list built from TV and movie subtitles) | Everyday spoken language | CC-BY-SA / GFDL / LGPL |
| Goethe-Institut A2/B1 word lists (optional) | Official exam vocabulary, used to check level labels | Check before use |

All sources are openly available. Attribution will be included in the dashboard and README.

## 6. Approach (data lifecycle)

1. **Collect:** download the datasets.
2. **Clean:** remove duplicates and proper nouns, and align spelling and word forms across sources.
3. **Model:** build one table of words with lemma, part of speech, gender, frequency rank, level and source.
4. **Analyse:** calculate cumulative coverage (what share of everyday text the top 500, 1,000 and 2,000 words cover) and compare the written and spoken lists.
5. **Visualise:** build the dashboard.
6. **Act:** export a "next 50 words" list for flashcard study (Anki).

## 7. Planned dashboard views

- Coverage curve: vocabulary size versus share of everyday text covered
- Filters by part of speech and level
- Noun gender overview
- Searchable word list with rank and level
- "Words to learn next" table

## 8. Tools

- SQL for data preparation
- Python (pandas) for cleaning and analysis
- Tableau Public for the dashboard (Power BI as an alternative)
- Git and GitHub for version control, issues and project board
- Anki for the flashcard export

## 9. Deliverables

- Cleaned dataset and documented data model
- Interactive dashboard, published online
- GitHub repository with a README explaining sources, steps and findings
- Short write-up of insights and limitations

## 10. Timeline (about 4 weeks, 4-6 hours per week)

| Week | Focus | Milestone |
|---|---|---|
| 1 | Data collection, exploration, cleaning | Clean dataset and data dictionary committed |
| 2 | Data model and analysis | Coverage table and 3 written findings |
| 3 | Dashboard build | Working dashboard with all core views |
| 4 | Testing, documentation, publishing | README finished, release v0.1 tagged |

Detailed tasks are tracked as GitHub issues on the project board.

## 11. Success criteria

- The dashboard answers the questions in section 4.
- Data sources and cleaning decisions are documented and reproducible.
- The "next 50 words" export works and is used in real study.

## 12. Risks and limitations

- Level labels (A2/B1) are estimates and may not match official exam lists exactly. They will be checked against the Goethe lists where possible.
- Frequency lists come from different text types (subtitles versus newspapers), so results will differ. The dashboard will show this explicitly.
- Some data noise is expected, such as proper nouns or odd word forms, and will be handled during cleaning.

## 13. Skills demonstrated

Data sourcing, SQL, Python data cleaning, data modelling, descriptive statistics, dashboard design, documentation, and building a tool for a defined user.