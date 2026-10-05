# Narke

A Socratic review skill that turns assumed understanding into explicit questions and a one-page list of unknowns.

**Status: concept and design stage.** The skill is not yet implemented or tested. Claude Code is the primary target; Codex support is planned.

## What Narke does

Narke reviews documents you write, read, or evaluate. Through a dialogue, it helps you identify what you cannot yet explain, support, or decide.

It combines two perspectives:

- **Fresh eyes:** ask what a reader needs to understand the document without sharing its unstated context.
- **Philosophical review:** examine definitions, distinctions, assumptions, evidence, inferences, and counterexamples.

## The dialogue

1. Read the document and establish the purpose of the review.
2. Ask a small set of questions tied to specific passages.
3. Use your answers to refine the questions and recognize what has been resolved.
4. Revisit both your assumptions and the reviewer's assumptions.
5. Produce a one-page list of the remaining unknowns.

The intended Claude Code command is:

```
/narke
```

Once implemented and installed, you will be able to provide a document or identify material already available in the conversation.

## The result

The final list will contain concise questions, their locations in the source, and the checks needed to answer them. Resolved questions will not remain on the unresolved list.

Narke will distinguish a gap in your understanding from a gap in the document, missing evidence, an undecided choice, or a limitation in the reviewer's own understanding.

Japanese output will use a concise writing guide inspired by ASD-STE100: one idea per sentence, consistent terms, explicit subjects, and clear conditions. ASD-STE100 is an English-language standard; this project does not claim Japanese-language compliance with it.

## Why “Narke”?

Ancient Greek *narkē* (νάρκη) refers to numbness and to an electric fish that causes it. The scientific genus name *Narke* comes from this word.

In Plato's *Meno*, Socrates is compared to an electric ray because his questions leave others perplexed. He also acknowledges his own perplexity. Narke carries that idea into document review: pause assumed understanding, make uncertainty explicit, and continue the inquiry together.

The gadfly, electric ray, and midwife guide the design: question assumptions, interrupt premature certainty, and help understanding take shape.

## Compatibility

The project will use a shared `SKILL.md` as its core. Installation and invocation instructions for Claude Code and Codex will be added after implementation and verification.

## License

MIT. Commercial use, modification, and redistribution are permitted, provided the copyright and permission notices are retained. See [LICENSE](LICENSE).

## References

- [Plato, Meno](https://classics.mit.edu/Plato/meno.html)
- [The ETYFish Project: Narkidae](https://etyfish.org/narkidae/)
- [ASD-STE100](https://www.asd-ste100.org/)
