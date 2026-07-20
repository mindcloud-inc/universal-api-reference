# <img src="https://images.mindcloud.co/apps/icons/sapling-128x128_1775075096279.png" alt="Sapling logo" width="28" height="28"> Sapling: Universal API

AI writing and language-processing API for grammar checking, autocomplete, paraphrasing, summarization, semantic search, and usage reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sapling/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sapling.ai/
- **Vendor API docs:** https://sapling.ai/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Dictionary Entries](actions/list-dictionary-entries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-dictionary-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Ai Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect AI-Generated Text](actions/detect-ai-generated-text.md) | GET | Detects whether text is AI-generated with Sapling. |

### Completion

| Action | Method | Description |
| --- | --- | --- |
| [Accept Completion](actions/accept-completion.md) | PUT | Records an accepted autocomplete completion in Sapling. |
| [Get Autocomplete](actions/get-autocomplete.md) | GET | Retrieves autocomplete suggestions for text from Sapling. |

### Custom Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Mapping](actions/add-custom-mapping.md) | POST | Adds a custom mapping in Sapling. |
| [List Custom Mappings](actions/list-custom-mappings.md) | GET | Retrieves configured custom mappings from Sapling. |
| [Remove Custom Mapping](actions/remove-custom-mapping.md) | DELETE | Deletes a custom mapping from Sapling. |

### Dictionary Entry

| Action | Method | Description |
| --- | --- | --- |
| [Add Dictionary Entry](actions/add-dictionary-entry.md) | POST | Adds a custom dictionary entry in Sapling. |
| [List Dictionary Entries](actions/list-dictionary-entries.md) | GET | Retrieves custom dictionary entries from Sapling. |
| [Remove Dictionary Entry](actions/remove-dictionary-entry.md) | DELETE | Deletes a dictionary entry from Sapling. |

### Edit

| Action | Method | Description |
| --- | --- | --- |
| [Get Edits](actions/get-edits.md) | GET | Retrieves grammar edits for text from Sapling. |
| [Get Spellcheck Suggestions](actions/get-spellcheck-suggestions.md) | GET | Retrieves spellcheck suggestions for text from Sapling. |

### Profanity Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Detect Profanity](actions/detect-profanity.md) | GET | Detects profanity in text with Sapling. |

### Rephrase Result

| Action | Method | Description |
| --- | --- | --- |
| [Expand Text](actions/expand-text.md) | GET | Expands text with additional detail using Sapling. |
| [Formalize Text](actions/formalize-text.md) | GET | Rewrites text in a more formal style with Sapling. |
| [Rewrite in Active Voice](actions/rewrite-in-active-voice.md) | GET | Rewrites text in active voice with Sapling. |
| [Split Sentences](actions/split-sentences.md) | GET | Splits text into shorter sentences with Sapling. |

### Sentiment Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Sentiment](actions/analyze-sentiment.md) | GET | Analyzes sentiment in text with Sapling. |

### Similar Terms

| Action | Method | Description |
| --- | --- | --- |
| [Get Similar Terms](actions/get-similar-terms.md) | GET | Retrieves similar terms for text from Sapling. |

### Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Text](actions/summarize-text.md) | GET | Summarizes input text into shorter output with Sapling. |

### Tone Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Detect Tone](actions/detect-tone.md) | GET | Detects tone in text with Sapling. |

