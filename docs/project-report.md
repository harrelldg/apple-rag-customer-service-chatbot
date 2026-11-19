# Apple Customer Service Assistant Project Report

> Accessible summary of the original course submission. Student identifiers have been removed.

## Team

Group 28: GUNAWAN Harrell Dave, RAHARDJO Marvel Reswanda, and WU Frederico Owen.

## Objective

Develop an AI-powered customer-service assistant for Apple in Hong Kong using retrieval-augmented generation, prompt engineering, and parameter tuning.

## Intended capabilities

- Answer frequently asked questions about features, troubleshooting, and specifications for products such as iPhone, Mac, and Apple Watch.
- Compare models, specifications, and pricing.
- Explain warranty, repair options, and official support procedures.
- Recommend products based on user needs, budget, and use cases.

## Knowledge base

The team collected and cleaned information primarily from Apple's official website, supplemented by selected third-party material. Experiments compared a non-RAG model, a RAG model with a small dataset, and a RAG model with an expanded dataset.

The expanded knowledge base covered product specifications, pricing, warranty, basic support guidance, FAQs, and Apple Store locations and opening hours.

## Prompt and parameter design

The team tested instruction design, variables, few-shot examples, and safety cases. Parameter presets included:

| Style | Temperature | Top-p | Other setting |
|---|---:|---:|---|
| Creative | 0.9 | 0.95 | Default output length |
| Balanced | 0.5 | 0.7 | Default output length |
| Precise | 0.2 | 0.4 | Default output length |
| Concise | Balanced configuration | Balanced configuration | Maximum 100 tokens |

## Findings

The expanded knowledge base produced more detailed responses. Balanced parameter settings were better suited to open-ended questions, while the hybrid system prompt encouraged structured, accurate, and user-friendly answers.

## Limitations

The original Dify.ai workspace is unavailable, so the prototype cannot be rerun or independently demonstrated from this repository. The report is preserved as evidence of the design and evaluation work rather than as deployable software.
