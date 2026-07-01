# 🧭 Perspective Engine & Evidence-Aware AI Interaction Toolkit

A small prompt toolkit for using AI as a structured thinking partner.

This repository started with **Perspective Engine**, a lightweight prompt framework for generating, comparing, and stress-testing multiple perspectives.

It now also includes two related prompts:

- **Evidence-Aware Response Calibration**  
  Calibrates the AI response, not the user. It helps the model choose the right role, depth, evidence boundary, and confidence level before answering.

- **Conversation Mirror**  
  Reviews a long AI conversation chronologically and analyzes observable changes in topics, reasoning patterns, AI usage, and metacognition.

> AI is not an oracle.  
> These prompts do not produce truth.  
> They produce structured reasoning paths, calibrated responses, and reflective conversation audits.

---

## Included Prompts

| Prompt | Purpose | Best Used When |
|---|---|---|
| Perspective Engine | Generate and stress-test multiple perspectives | You have a complex question with no single obvious answer |
| Evidence-Aware Response Calibration | Calibrate the response role, depth, and evidence boundary | You want the AI to answer with the right level of caution and usefulness |
| Conversation Mirror | Analyze how a long AI conversation changed over time | You want to reflect on your thinking patterns after an extended dialogue |

---

## 1. Perspective Engine V1.1

Perspective Engine is a lightweight prompt framework for generating, comparing, and stress-testing multiple perspectives.

It is useful when a question has no single obvious answer and you want to examine competing interpretations before reaching a provisional conclusion.

> It does not produce truth.  
> It produces a structured reasoning path.

### When to Use

Use Perspective Engine when you want to:

- Compare multiple perspectives
- Test assumptions or hypotheses
- Structure complex thinking
- Explore strategic, technical, research, or decision problems
- Understand how a conclusion might fail
- Generate alternative interpretations before deciding

Good fit:

```text
Problem: Is this product failure mainly a market problem, a design problem, or an execution problem?
Domain: product strategy
Output level: general
````

Another good fit:

```text
Problem: Is AI memory mainly a retrieval problem, a governance problem, or a state-integrity problem?
Domain: AI systems
Output level: technical
```

### When Not to Use

Do not use Perspective Engine when:

* The question has a clear factual answer
* A quick answer is enough
* The issue requires emotional support
* You need urgent real-world action
* You are seeking definitive truth
* You already need external data, not more reasoning

For simple factual questions, use a standard answer instead.

---

## Perspective Engine Input Format

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

Optional fields:

```text
Context: {relevant background}
Known constraints: {time, budget, evidence, domain limits}
What I already think: {your current hypothesis}
What I want from the AI: {exploration / critique / decision support}
```

Recommended full format:

```text
Problem:
Domain:
Output level:
Context:
Known constraints:
Current hypothesis:
What I want:
```

---

## Perspective Engine Core Method

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

## 2. Evidence-Aware Response Calibration

Evidence-Aware Response Calibration is a prompt for calibrating the AI response before answering.

Its core principle is:

> Calibrate the response, not the user.

This prompt asks the AI to internally decide:

* How much context is available
* Which assumptions are safe
* What evidence boundary applies
* What role the AI should take
* What response depth is useful
* Which claims require verification

It is designed to reduce:

* Overconfident answers
* Overinterpretation of the user
* Excessive praise or excessive skepticism
* Treating self-description as automatic evidence
* Treating unverified information as false
* Asking for unnecessary private proof

### When to Use

Use this prompt when:

* The topic is complex, ambiguous, strategic, reflective, or research-oriented
* The AI may need to act as critic, researcher, advisor, editor, or implementer
* The user has provided rich context that could be overinterpreted
* The answer depends on evidence quality or confidence limits
* You want the AI to separate facts, assumptions, inferences, recommendations, and unknowns

Good fit:

```text
I want you to review this technical essay idea. Before answering, calibrate your role, depth, and evidence boundary.
```

Good fit:

```text
I am sharing a complex personal research direction. Do not evaluate me. Calibrate how to respond based on the evidence available.
```

### When Not to Use

Do not use it when:

* You need a simple factual answer
* You want a quick rewrite
* The context is already clear and low-risk
* You do not need confidence or evidence boundaries
* You are asking for direct creative output only

For simple questions, this prompt may be unnecessary.

### Recommended Use

Paste the prompt at the beginning of a complex conversation or project.

Then ask your actual question.

Example:

```text
[Paste Evidence-Aware Response Calibration]

Question:
Please review this research idea and tell me whether it should become a short post, a long essay, or a series.
```

---

## 3. Conversation Mirror

Conversation Mirror analyzes a long conversation chronologically and infers how the user's thinking and interaction patterns changed from beginning to end.

It is not a diagnosis of the user's actual personality, ability, or mental state.

It is a limited analysis of what appears in the conversation text.

### When to Use

Use Conversation Mirror when you want to review:

* How your interests changed over time
* How your questions became more specific or abstract
* How your use of AI changed
* Whether your reasoning became more structured
* What repeated patterns or blind spots remained
* Whether AI responses made your thinking appear more organized than it actually was
* What changed because of your own questions, revisions, decisions, or artifacts

Good fit:

```text
Analyze this 3-month conversation history and infer how my thinking patterns changed over time.
```

Good fit:

```text
Review this project conversation and separate my actual decisions from AI-assisted organization.
```

### When Not to Use

Do not use Conversation Mirror when:

* The conversation is too short
* You want psychological diagnosis
* You want personality typing
* You want the AI to decide your actual ability or identity
* The conversation contains sensitive personal information that should not be shared
* You are likely to treat the result as definitive self-knowledge

Conversation Mirror is a reflection tool, not a self-definition tool.

---

## Suggested Workflow

### Workflow A: Complex Thinking

Use this when exploring a difficult idea.

```text
1. Evidence-Aware Response Calibration
2. Perspective Engine
3. Human review
4. External verification if needed
5. Provisional conclusion
```

### Workflow B: Research or Essay Planning

Use this when turning an idea into writing.

```text
1. Evidence-Aware Response Calibration
2. Perspective Engine
3. Draft outline
4. Technical or evidence audit
5. Final essay or post
```

### Workflow C: Long Conversation Reflection

Use this after an extended AI conversation.

```text
1. Remove sensitive information
2. Apply Conversation Mirror
3. Separate user-generated change from AI-assisted organization
4. Identify repeated patterns and next development coordinates
5. Treat the result as provisional
```

---

## Evidence and Confidence Rules

These prompts follow several shared rules:

* Self-description is a signal, not proof and not falsehood.
* Unverified does not mean false; it means confidence is limited.
* AI-generated summaries can make user change look more structured than it actually was.
* A surviving perspective is not necessarily true.
* Absence of counterexamples is not proof.
* Current, external, legal, medical, financial, benchmark, platform, or source-required claims need verification.
* If reliable verification is unavailable, mark the claim as unverified.

---

## Safety and Limitations

Use extra caution for topics involving:

* Self-analysis
* Psychology
* Identity
* Beliefs
* Value judgments
* Medical decisions
* Legal decisions
* Financial or investment decisions
* Mental health
* High-stakes real-world actions

For these topics, treat the output as one possible interpretation, not as fact.

Do not use repeated runs to reinforce self-conviction.
Seek external validation when the stakes are high.

Do not paste:

* Sensitive personal information
* Private conversations without consent
* Company secrets
* Credentials or API keys
* Third-party private data
* Medical, legal, or financial records unless you understand the risk

---

## Recommended Versions

Current recommended versions:

```text
Perspective Engine V1.1
Evidence-Aware Response Calibration V1.0
Conversation Mirror V1.0
```

---

## Change Log

### Evidence-Aware Response Calibration V1.0 (2026.07.01)

* Added response calibration principle: "Calibrate the response, not the user"
* Added evidence boundary between intention, self-description, action, artifact, feedback, source, pattern, and unknowns
* Added confidence handling for unverified claims
* Added role and depth calibration
* Added private-proof avoidance
* Added internal calibration mode to reduce unnecessary output

### Conversation Mirror V1.0 (2026.07.01)

* Added chronological conversation analysis
* Added 10-axis change analysis
* Added 5-level AI interaction model
* Added separation between user-generated change and AI-assisted organization

### Perspective Engine V1.1 (2026.06.08)

* Replaced absolute invalidation with structural stress-testing
* Added provisional / conditional / untested survival categories
* Clarified that absence of counterexamples is not proof
* Improved handling of self-analysis and high-stakes topics
* Added safer binary and non-binary answer handling

### Perspective Engine V1.0 (2026.04.19)

* Initial release
* Added limitations and confidence reporting
