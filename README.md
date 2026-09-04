## Embedded Risk Analytics · The Fathom Program

**Catch the step where an AI agent contradicts a decision it already made.**

Long-running agents rename a field, then keep writing the old name. They fix a bug, then reintroduce it. They commit an order, then commit it again. The run reports success, the tests pass, and the contradiction ships. Fathom reads the agent's own trace, folds the actions that succeeded into a ledger of committed state, and names the step where the agent broke faith with itself.

```
pip install fathom-read
fathom demo
```

| Repository | What it is |
|---|---|
| [fathom](https://github.com/ERA-Fathom/fathom) | Adapters and a CLI for the committed-state read over LangGraph, CrewAI, Letta, OpenInference (Arize Phoenix), DBOS, and coding-agent edit logs. Start here. |


**Send us a trace, get a readout.** Fifteen research pages and case studies, including the paper behind the read, are at [embeddedriskanalytics.com/research](https://embeddedriskanalytics.com/research.html). Paper: [SSRN 6683578](https://doi.org/10.2139/ssrn.6683578). Contact: [contact@embeddedriskanalytics.com](mailto:contact@embeddedriskanalytics.com).
