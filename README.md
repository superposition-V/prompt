# 🧭 Perspective Engine V1.1

Perspective Engine is a lightweight prompt framework for generating, comparing, and stress-testing multiple perspectives.

It is useful when a question has no single obvious answer and you want to examine competing interpretations before reaching a provisional conclusion.

> It does not produce truth.
> It produces a structured reasoning path.

---

## When to Use

Use Perspective Engine when you want to:

* Compare multiple perspectives
* Test assumptions or hypotheses
* Structure complex thinking
* Explore strategic, technical, research, or decision problems
* Understand how a conclusion might fail

Good fit:

```text
Problem: Is this product failure mainly a market problem, a design problem, or an execution problem?
```

---

## When Not to Use

Do not use it when:

* The question has a clear factual answer
* A quick answer is enough
* The issue requires emotional support
* You need urgent real-world action
* You are seeking definitive truth

For simple factual questions, use a standard answer instead.

---

## Input Format

```text
Problem: {your question}
Domain: {general / specialized}
Output level: {technical / general / introductory}
```

Only `Problem` is required.

Defaults:

```text
Domain: general
Output level: general
```

---

## Core Method

Perspective Engine follows this structure:

```text
Problem Redefinition
→ First Principle Reduction
→ Perspective Generation
→ Counterexample Testing
→ Survival Judgment
→ Confidence Evaluation
→ Reconstruction
→ Failure Conditions
```

Each perspective is stress-tested with counterexamples.

Survival does not mean truth.
It only means the perspective was not defeated under the stated assumptions and tests.

---

## Warning

Use extra caution for topics involving:

* Self-analysis
* Psychology
* Identity
* Beliefs
* Value judgments
* Medical, legal, financial, or mental health decisions

For these topics, treat the output as one possible interpretation, not as fact.

Do not use repeated runs to reinforce self-conviction.
Seek external validation when the stakes are high.

---

## Confidence Levels

* **Strong**: structurally robust within the given assumptions
* **Moderate**: conditionally valid
* **Weak**: requires further validation

Confidence is comparative and provisional, not absolute.

---

## Recommended Version

Current recommended version:

```text
Perspective Engine V1.1
```

V1.0 is preserved for reference but is no longer recommended.

---

## Change Log

### V1.1 (2026.06.08)

* Replaced absolute invalidation with structural stress-testing
* Added provisional / conditional / untested survival categories
* Clarified that absence of counterexamples is not proof
* Improved handling of self-analysis and high-stakes topics
* Added safer binary and non-binary answer handling

### V1.0 (2026.04.19)

* Initial release
