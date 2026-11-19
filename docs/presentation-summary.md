# Presentation Summary

## Project goal

The presentation introduced a Hong Kong-focused Apple customer-service assistant built in Dify.ai. The prototype was designed to answer frequently asked questions, compare Apple products, provide support guidance and recommend products according to user needs.

## Knowledge base

The team assembled approximately 18 Apple product and support documents. The material covered product specifications, Hong Kong pricing, warranties, FAQs, support information and Apple Store locations. These sources supplied the retrieved context used by the RAG workflow.

## RAG comparison

The team compared three configurations:

1. A language model without retrieval-augmented generation.
2. RAG with a small initial knowledge base.
3. RAG with the expanded product and support knowledge base.

The expanded knowledge base produced the strongest example response: it was more specific to the user's request and cited relevant source material. The comparison illustrated how broader, relevant retrieved context can improve answer detail and grounding.

## Generation parameters

Four response styles were explored:

| Preset | Configuration |
| --- | --- |
| Creative | Temperature 0.9; top-p 0.95 |
| Balanced | Temperature 0.5; top-p 0.7 |
| Precise | Temperature 0.2; top-p 0.4 |
| Concise | Maximum 100 output tokens |

The balanced configuration shown in the presentation used `qwen-max`, temperature 0.5, top-p 0.7 and a 512-token output limit. The team found that balanced settings supported readable answers without making them overly rigid or overly variable.

## Prompt and safety design

The system prompt combined an Apple customer-service role, instructions to rely on the knowledge base, few-shot examples, actionable support guidance and refusal behaviour for unsafe or off-topic requests. Safety examples included requests involving access to a lost device and jailbreaking. The resulting hybrid prompt improved response structure and reliability in the demonstrated examples.

## Takeaways

- A broader, relevant knowledge base improved answer specificity and source grounding.
- Balanced generation parameters supported clear and readable responses.
- Role instructions, examples and explicit boundaries improved consistency and safe behaviour.
- RAG evaluation should consider both response quality and the relevance of retrieved context.

## Scope

This document summarises the academic presentation. It does not provide the original slides, deployable source code, a live chatbot or access to the former Dify workspace.
