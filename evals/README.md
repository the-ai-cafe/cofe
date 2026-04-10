
# COFE Evaluations

Evaluations organized by rubric version. Each version subfolder contains evaluations run against that version of the COFE rubric.

## Versions

### [v1.2/](v1.2/) — Initial inter-rater study (April 7, 2026)

**Target:** Verification Gates Design Brief — a system design document for a multi-layer verification architecture in an AI agent pipeline. Same document evaluated by all evaluators using the same rubric and prompt.

| # | Evaluator | Type | System Score | Label |
|---|-----------|------|-------------|-------|
| 1 | [Claude Opus 4.6](v1.2/01_claude_opus_system_eval.md) | System (internal) | 4.34 | Strong |
| 2 | [DeepSeek R1](v1.2/02_deepseek_r1_system_eval.md) | System (external) | 4.00 | Strong |
| 3 | [DeepSeek R1 v2](v1.2/03_deepseek_r1_v2_system_eval.md) | System (external) | 4.68 | Excellent |
| 4 | [Grok 3](v1.2/04_grok3_system_eval.md) | System (external, self-eval) | 5.00 | Excellent |
| 5 | [Gemini](v1.2/05_gemini_system_eval.md) | Output + System (external) | 4.70 | Excellent |
| 6 | [ChatGPT](v1.2/06_chatgpt_system_eval.md) | System (external, limited context) | 3.88 | Strong |
| 7 | [Human (system builder)](v1.2/08_human_system_eval.md) | System (full operational context) | 3.76 | Strong |
| 8 | [DeepSeek R1 — COFE-on-CLEAR](v1.2/07_deepseek_r1_cofe_on_clear.md) | Meta-evaluation (v1.3.1 rubric, different target) | 2.94 | Developing |

## Inter-Rater Findings

The 8-evaluator study (seven on the same target, one meta-evaluation on a different framework) revealed:

- **Score gradient maps to available context.** Evaluators with more operational context scored lower (more accurate). Evaluators with only the design documents scored higher.
- **Execution monitoring is the convergent gap.** 4 of 7 evaluators scored Operation mechanism #3 (execution monitoring) at 2-3. The exception (Grok, score 5) conflated component existence with mechanism effectiveness.
- **COFE evaluates evaluations.** The framework's own criteria diagnose where each evaluation diverges — making evaluator reasoning legible and auditable.
- **Human evaluator scored lowest Efficiency (2.30) and second-lowest composite (3.76).** The system builder knows the verification works (he watches it catch errors) and knows cost management doesn't exist (he pays the token bills). This split is only available to the operator — and it's the strongest evidence that context depth drives evaluation accuracy.

## How to Read These

Each evaluation follows a consistent format:
1. **Metadata** — evaluator, date, COFE version, target, evaluation type
2. **Score Summary** — all scores in one table
3. **Phase Details** — per-mechanism scores with reasoning
4. **Key Findings** — strengths, gaps, recommendations

These are real evaluations, not demonstrations. Scores reflect genuine assessment, including where the evaluators disagree.
