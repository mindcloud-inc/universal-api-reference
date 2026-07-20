# Datamuse: Native API Reference

A consolidated summary of Datamuse's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.datamuse.com/api/
- **API base URL:** `https://api.datamuse.com`

## Authentication

### No authentication

The Datamuse API is a public read-only service and does not require an API token for the selected endpoints.

This API does not require request authentication.

[Official authentication documentation](https://www.datamuse.com/api/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `max` in the query string to set the page size (default 10; accepted range 1–1000).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Adjectives For Noun](actions/find-adjectives-for-noun.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Antonyms](actions/find-antonyms.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Consonant Matches](actions/find-consonant-matches.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Contextual Words](actions/find-contextual-words.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Frequent Followers](actions/find-frequent-followers.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Frequent Predecessors](actions/find-frequent-predecessors.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Homophones](actions/find-homophones.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Kind Of Words](actions/find-kind-of-words.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find More Specific Words](actions/find-more-specific-words.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Nouns For Adjective](actions/find-nouns-for-adjective.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Part Terms](actions/find-part-terms.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Synonyms](actions/find-synonyms.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Triggered Words](actions/find-triggered-words.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Whole Terms](actions/find-whole-terms.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Words By Meaning](actions/find-words-by-meaning.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Words By Spelling Pattern](actions/find-words-by-spelling-pattern.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Find Words That Sound Like](actions/find-words-that-sound-like.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Get Spanish Word Suggestions](actions/get-spanish-word-suggestions.md) | `GET /sug` | [docs](https://www.datamuse.com/api/) |
| [Get Word Metadata](actions/get-word-metadata.md) | `GET /words` | [docs](https://www.datamuse.com/api/) |
| [Get Word Suggestions](actions/get-word-suggestions.md) | `GET /sug` | [docs](https://www.datamuse.com/api/) |
