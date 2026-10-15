# German Vocabulary Dashboard

An interactive dashboard of the most common German words, built to help learners move from A2 to B1 by studying the words that matter most first.

**Status:** In progress (planning phase). First prototype planned for the end of week 4.

## What it will show

- How much everyday German a learner understands at 500, 1,000, 2,000 and 3,000 words
- The most frequent words by part of speech and level (A2 / B1)
- Noun gender patterns (der / die / das)
- A "next 50 words to learn" list that can be exported to Anki

## Why this project

Frequency lists are a popular way to learn vocabulary, but they are usually long tables with no sense of progress. This project turns open data into something a learner can explore and act on. The first user is the author, who is learning German.

## Data sources

| Source | Used for | Licence |
|---|---|---|
| wordhoard | Lemmas, part of speech, frequency rank, noun gender, estimated CEFR level | CC-BY-SA-4.0 |
| Wiktionary frequency list (TV and movie subtitles) | Everyday spoken-language frequency | CC-BY-SA / GFDL / LGPL |
| Goethe-Institut A2/B1 word lists (optional) | Checking level labels | See source |

Please credit these sources if you reuse any derived data.

## Tools

SQL, Python (pandas), Tableau Public (or Power BI), Git/GitHub, Anki.

## Repository structure

```
├── README.md
├── docs/
│   ├── project-proposal.md      # goals, scope, timeline, risks
│   ├── data-dictionary.md       # (to be added) what each column means
│   └── decisions/               # (to be added) short notes on key choices
├── data/
│   ├── raw/                     # downloaded files, untouched
│   └── processed/               # cleaned files
├── notebooks/                   # exploration and analysis
├── sql/                         # queries
└── dashboard/                   # screenshots, workbook, export files
```

## Documentation

- [Project proposal](docs/project-proposal.md)

## Roadmap

| Week | Focus |
|---|---|
| 1 | Data collection, exploration, cleaning |
| 2 | Data model and analysis |
| 3 | Dashboard build |
| 4 | Testing, documentation, release v0.1 |

Progress is tracked on the project board in this repository.

## How to reproduce

*To be completed once the pipeline is built (setup steps, how to download the data, how to run the notebooks).*

## Findings

*To be completed after the analysis.*

## Limitations

- Level labels (A2/B1) are estimates and may differ from official exam lists.
- Spoken-language and written-language frequency lists differ, and results depend on which is used.

## Licence

Code: MIT. Data: see the licences of the sources above.

## Author

Chaitanya Nair. Data analyst, based in Stuttgart.# german-vocab-dashboard