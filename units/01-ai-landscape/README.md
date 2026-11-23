# Unit 01 — The AI Landscape

## Objective

By the end of this unit, you should be able to explain the relationships among artificial intelligence (AI), machine learning (ML), deep learning (DL), and generative AI, and classify practical examples correctly.

## 1. The conceptual map

These terms are related, but they are not interchangeable:

- **Artificial intelligence:** the broad field of building systems that perform tasks associated with intelligent behavior.
- **Machine learning:** a subset of AI in which a system learns patterns from data rather than relying only on explicitly programmed rules.
- **Deep learning:** a subset of ML based on neural networks with multiple layers.
- **Generative AI:** systems that generate new content, such as text, images, audio, video, or code. Many current generative systems use deep learning, but the term describes a capability and application family rather than one single architecture.

A useful mental model is:

```text
Artificial Intelligence
└── Machine Learning
    └── Deep Learning
        └── Many modern Generative AI systems
```

This diagram is intentionally simplified: generative AI is not strictly a taxonomic child of deep learning in every possible definition. It is a capability that is commonly implemented with deep neural networks today.

## 2. How the approaches differ

### Rule-based software

A developer specifies explicit rules. Given the same input and rules, behavior is generally predictable.

Example: reject a transaction when its amount exceeds a configured limit.

### Machine learning

A model is fitted to examples. During training, an algorithm adjusts model parameters to reduce a defined error or loss.

Example: estimate the probability that a transaction is fraudulent based on historical labeled transactions.

### Generative AI

A trained model produces a new output conditioned on an input or context.

Example: generate a draft explanation of why a transaction was flagged, using relevant policy documents.

## 3. Training versus inference

**Training** is the process of using data and an optimization procedure to determine model parameters. It can be computationally expensive and is usually performed separately from normal application requests.

**Inference** is the use of an already-trained model to produce predictions or generated outputs for new inputs.

In an application, the typical flow is:

1. Receive input.
2. Validate and prepare it.
3. Send it to a model.
4. Receive the model output.
5. Validate, interpret, and use the output.

Do not assume that every AI application trains its own model. Many production applications call an existing model through an API or run a pretrained model locally.

## 4. Important vocabulary

| Term | Meaning |
|---|---|
| Dataset | A collection of examples used for training, validation, or testing |
| Feature | An input variable used by a model |
| Label | The expected target in a supervised-learning example |
| Model | A parameterized computational system that maps inputs to outputs |
| Parameter | A learned value inside a model |
| Training | The process of fitting model parameters |
| Inference | Using a trained model |
| Loss | A numerical measure of model error for an optimization objective |
| Generalization | The ability to perform well on examples not used for training |

## 5. Guided exercise: classify the system

Classify each example as rule-based software, machine learning, or generative AI. Some real systems combine more than one approach.

1. A service blocks a payment when the amount exceeds a fixed threshold.
2. A model estimates whether a payment is fraudulent from historical examples.
3. An assistant drafts a natural-language summary of a support ticket.
4. A document-processing pipeline uses OCR, a classifier, and fixed validation rules.

Write your answers and justify each classification in your own words.

## 6. Practical experiment

Create a file named `experiments/01_ai_landscape.md` and record:

- One real-world example of rule-based software.
- One real-world example of machine learning.
- One real-world example of generative AI.
- For each example, identify its input, output, and where a human or deterministic validation step should remain.

## 7. Independent challenge

Choose a banking, e-commerce, or customer-support workflow. Design a solution that combines deterministic rules and an ML or generative AI component.

Document:

- The business problem.
- Which decisions must remain deterministic.
- Which task could benefit from ML or generative AI.
- What data the model would need.
- How you would validate the output.
- What failure mode would require human review.

Do not use an LLM to write the challenge answer. The goal is to test your own understanding.

## 8. Knowledge check

Answer without looking at the theory:

1. Is every machine-learning system generative AI? Explain.
2. Is every generative AI system necessarily a large language model?
3. What is the difference between training and inference?
4. Why can a system combine deterministic rules with a learned model?
5. Why is evaluation on unseen data important?

## Completion criteria

You can explain the four concepts accurately, classify the examples with defensible reasoning, and complete the independent challenge. Save your answers in your experiment report and commit them to your repository.

## References

- [NIST — Artificial Intelligence](https://www.nist.gov/artificial-intelligence)
- [Google Machine Learning Crash Course — ML concepts](https://developers.google.com/machine-learning/crash-course)
- [Stanford Encyclopedia of Philosophy — Artificial Intelligence](https://plato.stanford.edu/entries/artificial-intelligence/)
