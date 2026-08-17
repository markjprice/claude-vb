---
name: blog-post-social-summary
description: Turns a published blog post into a short, factual three-sentence social summary ending in a call to action. Only use this skill when the user explicitly asks for a "social summary" of a blog post or explicitly names this skill (e.g. "give me a social summary of this post," "run the blog post social summary skill on this"). Do not use it for general summarization, longer recaps, or other content-repurposing requests where the user hasn't explicitly asked for a social summary.
---

# Blog Post Social Summary

Turns a published blog post into a tight, three-sentence summary suitable for sharing on social media, ending in a clear call to action. The whole point is trustworthiness: every claim in the output must be traceable back to the source, so a reader can act on it with confidence.

## Inputs

Two things are required before drafting:

1. **The blog post itself** — pasted text, an uploaded document, or an accessible link. If it's a link, fetch it to get the actual content; don't summarize from the link text alone.
2. **The target audience** — who the summary is for (e.g. "new customers," "event attendees"). This shapes what counts as the main point and which facts matter most.

One thing is optional:

3. **A preferred call to action** — if the user doesn't give one, use an action stated in the source itself (e.g. "register," "read more," "sign up").

If either required input is missing, ask one focused question for the single most important missing piece — don't guess, and don't ask about more than one thing at once.

## Steps

1. Read the source and identify its main point, its target audience, and the next action it wants the reader to take.
2. List the source facts that support the main point. This working list is what you'll check the draft against later — keep it handy.
3. Draft exactly three sentences. The call to action goes in the final sentence.
4. Check every factual claim in the draft against the source. If anything doesn't trace back to the source, cut or fix it. Then return the summary only — no preamble, no explanation, no restatement of the input.

## Rules

- Use plain, professional language. Don't add hashtags or emoji unless the user asks for them.
- Never invent facts, quotations, dates, links, offers, or benefits. If the source doesn't say it, it doesn't go in the summary — precision here is what makes the output usable without a human having to double-check it.
- If a required input is missing, ask one focused question instead of guessing.

## Example

**Input (condensed):** BrightDesk will hold free 30-minute online setup clinics every Wednesday at 2:00 p.m. ET, starting August 12. Customers can bring one setup question. Registration is required.

**Output:**
Need help setting up BrightDesk? Free 30-minute online clinics begin August 12 and run every Wednesday at 2:00 p.m. ET. Register for a clinic and bring one setup question.

## Acceptance criteria

Before returning the summary, confirm:

- The output contains exactly three sentences.
- The final sentence contains one clear call to action.
- Every factual claim can be traced to the source.
