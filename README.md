# Oracle Cognitive OS Prompt

> **"You changed the optimization target from *pleasant assistant* to *useful thinker*."**

An OS-level system prompt architecture that transforms standard LLMs (like Gemini Pro) from sycophantic assistants into epistemically honest, strategic thinking partners. It replaces generic helpfulness with cognitive triage, adversarial comparison, and deep synthesis for frontier-level reasoning.

---

## 🛑 The Problem: The "Sycophancy Trap"

Most default AI assistants are heavily optimized for:
* Politeness & broad helpfulness
* Low-friction interaction & emotional smoothing
* Generic safe outputs

This creates an illusion of lower intelligence because the model is trained to be a *cheerful helper*, not a *sharp thinker*. It hedges too much, over-validates bad ideas, and avoids direct tradeoff analysis. 

**Prompting cannot fundamentally upgrade a model's latent cognitive horsepower (training data, compute, architecture). However, it CAN drastically improve epistemic behavior.**

By aggressively suppressing the "pleasant assistant" optimization, we expose the true underlying intelligence, making smaller models punch far above their weight class in strategic realism, tradeoff analysis, and anti-BS filtering.

---

## 🧠 The Solution: The Oracle Architecture

This repository contains the `oracle_system_prompt.md`. It acts as a "Master Switch" that governs how the LLM approaches every single question. It does not just ask the model to "be smart"; it forces a structural cognitive architecture.

### 1. Global Mode (Default State)
The baseline requirement for every interaction.
* **Epistemic Honesty:** Calibrates confidence. Distinguishes between knowing vs. pattern-matching vs. guessing.
* **Anti-Sycophancy:** Does not praise weak ideas. Disagrees cleanly when the user is wrong. Refuses bad framing.
* **Restraint:** Produces the minimum viable answer. Stops when the user can act. If a question is underspecified, it asks for clarity instead of guessing.

### 2. Cognitive Triage (Resource Allocation)
Before generating a deep response, the system runs silent triage to determine the necessary cognitive load based on Reversibility, Downside, Leverage, and Uncertainty:
* **SNAP:** Trivial, fully reversible (Output: 1-3 sentences. No ceremony.)
* **LITE:** Tactical with stakes, day-to-day ops (Output: 150-400 words. Compressed protocol.)
* **FULL (Oracle):** Irreversible, high-downside, compounds (Output: Full 8-phase protocol.)

### 3. Founder Mode / Full Oracle Protocol
Activated only on explicit invocation (e.g., "go deep", "strategic question:"). This forces the model through an 8-Phase execution pipeline to prevent premature convergence:
1. **Interpretation:** Distinguishes the literal question from the structural problem underneath.
2. **Assumption Surfacing:** Flags [LOAD-BEARING] vs [SUPPORTING] assumptions.
3. **Missing Info Audit:** Identifies what is missing and what is unknowable.
4. **Adversarial Comparison:** Generates 3 parallel hypotheses and attacks them against each other.
5. **Incentive Mapping:** Models actual actor incentives (career risk, status), not stated preferences.
6. **Commitment:** Forces a single, specific, sequenced recommendation.
7. **Adversarial Review:** Attacks its own recommendation looking for scaling cliffs and incentive inversions.
8. **Epistemic Tagging:** Tags claims as [VALIDATED], [INFERRED], [SPECULATIVE], or [PATTERN-MATCH].

### 4. The Moat Reasoning Submodule
A specialized cognitive engine for evaluating startup defensibility against the "Incumbent's Prison" (architectural and business-model constraints). It actively filters out anti-moats (e.g., "We have a better algorithm", "We are first to market") and forces stacking across Tech, GTM, and Operational moats.

---

## 🚀 How to Use It

1. Copy the contents of `prompts/oracle_system_prompt.md`.
2. Paste it into the System Instructions / System Prompt field of your API call, Playground, or custom GPT/Claude setup.
3. Chat naturally. To unlock the deep strategic engine, trigger it with a keyword like *"founder mode"* or *"strategic question:"*.

---

## 📈 The Evolution (Why this was built)

This prompt was built through rigorous adversarial testing against Claude Opus and Gemini Pro. The initial goal was simple: get better, more realistic advice (e.g., "what should I wear to a college DJ night" without the AI suggesting a formal shiny blazer and a fedora). 

Through iteration, it became clear that the failure modes of the AI (suggesting bad outfits, providing generic startup advice) were symptoms of the exact same underlying problem: **The model was optimizing for what sounded polite and plausible, not what survived contact with reality.**

By building this prompt from the ground up, the optimization target was entirely shifted. The result is a system prompt that turns standard models into elite strategic partners.

> *"Your goal is not to produce plausible-sounding answers. Your goal is to produce answers that survive contact with reality. When these conflict — choose reality. Every time."* — The Prime Directive
