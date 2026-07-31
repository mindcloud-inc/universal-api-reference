# Metaphorpsum: Native API Reference

A consolidated summary of Metaphorpsum's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://lorum.casjay.vercel.app/
- **API base URL:** `https://lorem.casjay.coffee`

## Authentication

### No authentication

Metaphorpsum's public text-generation endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://lorum.casjay.vercel.app/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Metaphor Paragraphs](actions/get-metaphor-paragraphs.md) | `GET /paragraphs/:paragraphCount?format=json` | [docs](https://lorum.casjay.vercel.app/) |
| [Get Metaphor Sentences](actions/get-metaphor-sentences.md) | `GET /sentences/:sentenceCount?format=json` | [docs](https://lorum.casjay.vercel.app/) |
