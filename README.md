## Embedded Risk Analytics · The Fathom Program

**Catch the step where an AI agent contradicts a decision it already made, and read how much functional life the run has left.**

Long-running agents rename a field, then keep writing the old name. They fix a bug, then reintroduce it. They commit an order, then commit it again. The run reports success, the tests pass, and the contradiction ships. Fathom reads the agent's own trace, folds the actions that succeeded into a ledger of committed state, and names the step where the agent broke faith with itself.

**The expiry read.** Every agent run spoils eventually. From the same trace, Fathom reports how many steps a run has left before its committed state contradicts itself, and raises an alarm while a rejected or corrupted action stands in the record. The read moves when the agent acts and stays flat while it only looks, and a wall clock enters nowhere.

```
pip install fathom-read
fathom demo                 # the committed-state read on the bundled example
fathom read chatdev.log     # the read on a framework's own log file, format recognised
fathom expiry trace.json    # functional life remaining, and the exposure alarm
```

| Repository | What it is |
|---|---|
| [fathom](https://github.com/ERA-Fathom/fathom) | Adapters and a CLI for the committed-state read and the expiry read. Fourteen formats: LangGraph, CrewAI, Letta, OpenInference (Arize Phoenix), DBOS and coding-agent edit logs by export, and the log files ChatDev, MetaGPT, OpenManus, Magentic-One, HyperAgent, AppWorld and AG2 already write, read as they are. Start here. |

**Send us a trace, get a readout.** Fifteen research pages and case studies, including the paper behind the read, are at [embeddedriskanalytics.com/research](https://embeddedriskanalytics.com/research.html). Paper: [SSRN 6683578](https://doi.org/10.2139/ssrn.6683578). Contact: [contact@embeddedriskanalytics.com](mailto:contact@embeddedriskanalytics.com).
