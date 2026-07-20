# <img src="https://images.mindcloud.co/apps/icons/free-dictionary-icon_1775760837393.png" alt="Free Dictionary logo" width="28" height="28"> Free Dictionary: Universal API

Free Dictionary wraps the public Free Dictionary API so you can look up English word definitions, phonetics, origins, examples, synonyms, and antonyms.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freeDictionary/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dictionaryapi.dev/
- **Vendor API docs:** https://dictionaryapi.dev/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Word Entries](actions/get-word-entries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeDictionary/latest/actions/get-word-entries?connectionId=$CONNECTION_ID&language=string&word=example%3A%20hello" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Dictionary Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Word Entries](actions/get-word-entries.md) | GET |  |
| [Get Word Entries (Legacy v1)](actions/get-word-entries-legacy-v1.md) | GET |  |

