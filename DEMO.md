# OrbitTech Evaluation Console

The local UI is a presentation aid for this lab. It does not replace the
required command-line pipeline or alter any benchmark artifact.

```powershell
.\.venv\Scripts\python.exe demo_app.py
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in a browser. Use another
port if needed:

```powershell
.\.venv\Scripts\python.exe demo_app.py --port 8080
```

Suggested demo flow:

1. Start with the quality profile: 20 cases, five metrics, 60% pass rate.
2. Inspect `A02` to show the retrieval trace, safe refusal, and the lexical
   metric false-positive discussed in `reflection.md`.
3. Inspect `M06` to contrast high relevance with low faithfulness and
   completeness.
4. Edit a saved answer and press **Evaluate answer** to demonstrate the
   evaluation engine separately from generation.
5. Optionally use **Live RAG playground**. It needs `OPENAI_API_KEY` and
   `OPENAI_MODEL` in the local `.env`; it calls only `DomainAssistant` and
   never consults the golden expected answer.

The dashboard reads `artifacts/benchmark_results.json` and
`artifacts/actual_answers.json`; regenerate the normal pipeline artifacts
before a presentation if you want to show a new run.
