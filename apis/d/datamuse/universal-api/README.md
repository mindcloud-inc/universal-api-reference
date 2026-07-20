# <img src="https://images.mindcloud.co/apps/icons/datamuse-logo-rgb_1781650565796.png" alt="Datamuse logo" width="28" height="28"> Datamuse: Universal API

Datamuse is a public word-finding API for lexical search, autocomplete, spelling, sound-alike, context, and related-word lookups.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datamuse/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datamuse.com/
- **Vendor API docs:** https://www.datamuse.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Find Adjectives For Noun](actions/find-adjectives-for-noun.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-adjectives-for-noun?connectionId=$CONNECTION_ID&noun=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Spanish Word Suggestions

| Action | Method | Description |
| --- | --- | --- |
| [Get Spanish Word Suggestions](actions/get-spanish-word-suggestions.md) | GET | Retrieves Spanish word suggestions from Datamuse for partial search text. |

### Word Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Word Metadata](actions/get-word-metadata.md) | GET | Retrieves Datamuse metadata for a word by exact spelling. |

### Word Results

| Action | Method | Description |
| --- | --- | --- |
| [Find Adjectives For Noun](actions/find-adjectives-for-noun.md) | GET | Finds adjectives that often describe a noun in Datamuse. |
| [Find Antonyms](actions/find-antonyms.md) | GET | Finds antonyms in Datamuse for a given word. |
| [Find Consonant Matches](actions/find-consonant-matches.md) | GET | Finds consonant matches in Datamuse for a given word. |
| [Find Contextual Words](actions/find-contextual-words.md) | GET | Finds contextual words in Datamuse by sentence context. |
| [Find Frequent Followers](actions/find-frequent-followers.md) | GET | Finds words that frequently follow a given word in Datamuse. |
| [Find Frequent Predecessors](actions/find-frequent-predecessors.md) | GET | Finds words that frequently precede a given word in Datamuse. |
| [Find Homophones](actions/find-homophones.md) | GET | Finds homophones in Datamuse for a given word. |
| [Find Kind Of Words](actions/find-kind-of-words.md) | GET | Finds what a word is a kind of in Datamuse. |
| [Find More Specific Words](actions/find-more-specific-words.md) | GET | Finds more specific words in Datamuse for a given word. |
| [Find Nouns For Adjective](actions/find-nouns-for-adjective.md) | GET | Finds nouns often described by an adjective in Datamuse. |
| [Find Part Terms](actions/find-part-terms.md) | GET | Finds wholes a part term belongs to in Datamuse. |
| [Find Synonyms](actions/find-synonyms.md) | GET | Finds synonyms in Datamuse for a given word. |
| [Find Triggered Words](actions/find-triggered-words.md) | GET | Finds words in Datamuse strongly associated with a given word. |
| [Find Whole Terms](actions/find-whole-terms.md) | GET | Finds parts a whole term comprises in Datamuse. |
| [Find Words By Meaning](actions/find-words-by-meaning.md) | GET | Finds words in Datamuse by related meaning. |
| [Find Words By Spelling Pattern](actions/find-words-by-spelling-pattern.md) | GET | Finds words in Datamuse by spelling pattern. |
| [Find Words That Sound Like](actions/find-words-that-sound-like.md) | GET | Finds words in Datamuse by pronunciation similarity. |

### Word Suggestions

| Action | Method | Description |
| --- | --- | --- |
| [Get Word Suggestions](actions/get-word-suggestions.md) | GET | Retrieves Datamuse word suggestions for partial search text. |

