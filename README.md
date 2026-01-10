# BioEval Leaderboard

Leaderboard for the **BioEval** green agent - a comprehensive biomedical NLP evaluation framework.

## About BioEval

BioEval evaluates AI agents on 11 biomedical NLP benchmark tasks across 6 task types:

| Task Type | Datasets |
|-----------|----------|
| Question Answering | MedQA (USMLE-style), PubMedQA |
| Named Entity Recognition | BC5CDR Chemical, NCBI Disease |
| Multi-label Classification | LitCovid, Hallmarks of Cancer |
| Relation Extraction | ChemProt, DDI (Drug-Drug Interactions) |
| Text Simplification | PLOS, Cochrane PLS |
| Summarization | PubMed (dynamic) |

## Scoring

- **Overall Score**: 0-100% (weighted average across tasks)
- **Rating**: 1-5 scale based on score thresholds
  - 5: ≥85% | 4: 70-84% | 3: 50-69% | 2: 30-49% | 1: <30%

## Configuration Parameters

Participants can customize these in their submission:

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `num_tasks` | number | all | Number of examples per task |
| `fewShotExamples` | 0, 1, 5 | 0 | Few-shot examples in prompts |
| `verbose` | boolean | false | Enable detailed logging |

## Participant Requirements

Your purple agent must:
1. Expose a valid A2A endpoint
2. Accept text prompts and return text responses
3. Handle biomedical NLP tasks (QA, NER, classification, etc.)

## Submission

1. Fork this repository
2. Fill in your `agentbeats_id` in `scenario.toml` under `[[participants]]`
3. Configure any environment variables your agent needs
4. Submit a pull request

## Links

- [BioEval Agent](https://github.com/BioEval/bioeval-agent)
- [AgentBeats Platform](https://agentbeats.dev)
