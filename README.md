## Right Rudder · by Embedded Risk Analytics

**Catch the step where an AI agent contradicts a decision it already made, and read how much functional life the run has left.**

Long-running agents rename a field, then keep writing the old name. They fix a bug, then reintroduce it. They commit an order, then commit it again. The run reports success, the tests pass, and the contradiction ships. Right Rudder reads the agent's own trace, folds the actions that succeeded into a ledger of committed state, and names the step where the agent broke faith with itself.

**The expiry read.** Every agent run spoils eventually. From the same trace, Right Rudder reports how many steps a run has left before its committed state contradicts itself, and raises an alarm while a rejected or corrupted action stands in the record. The read moves when the agent acts and stays flat while it only looks, and a wall clock enters nowhere.

```
pip install right-rudder
right-rudder demo                 # the committed-state read on the bundled example
right-rudder read chatdev.log     # the read on a framework's own log file, format recognised
right-rudder expiry trace.json    # functional life remaining, and the exposure alarm
```

| Repository | What it is |
|---|---|
| [right-rudder](https://github.com/RightRudderAI/right-rudder) | Adapters and a CLI for the committed-state read and the expiry read, over fifteen trace formats. Start here. |
| [coherence-census](https://github.com/RightRudderAI/coherence-census) | Every framework the read has run on, what it caught, and a trace that replays each catch in one command. |
| [langchain-right-rudder](https://github.com/RightRudderAI/langchain-right-rudder) | The read and the repair as LangChain agent middleware. |
| [right-rudder-openshell](https://github.com/RightRudderAI/right-rudder-openshell) | The read for agents in NVIDIA OpenShell sandboxes, joined to the platform's own delivery record. |
| [right-rudder-prime-agent](https://github.com/RightRudderAI/right-rudder-prime-agent) | The read over Prime Agent sessions, the orchestrator's and its children's. |
| [right-rudder-foreman](https://github.com/RightRudderAI/right-rudder-foreman) | The read on Foreman runs, beside the Jev verification loop. |
| [jev-coherence-bench](https://github.com/RightRudderAI/jev-coherence-bench) | A benchmark that sets the committed-state read against a typed verifier. |

Right Rudder was called Fathom until October 2026. The old package names, `fathom-read` and `langchain-fathom`, now install the new ones.

**Send us a trace, get a readout.** Research pages and case studies, including the paper behind the read, are at [embeddedriskanalytics.com/research](https://embeddedriskanalytics.com/research.html). Paper: [SSRN 6683578](https://doi.org/10.2139/ssrn.6683578). Contact: [contact@embeddedriskanalytics.com](mailto:contact@embeddedriskanalytics.com).
