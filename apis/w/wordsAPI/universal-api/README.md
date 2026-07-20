# <img src="https://images.mindcloud.co/apps/icons/words-api_1776006227286.png" alt="WordsAPI logo" width="28" height="28"> WordsAPI: Universal API

Dictionary and lexical lookup actions for WordsAPI via RapidAPI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wordsAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wordsapi.com/docs/
- **Vendor API docs:** https://www.wordsapi.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Word](actions/get-word.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wordsAPI/latest/actions/get-word?connectionId=$CONNECTION_ID&word=soliloquy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Word

| Action | Method | Description |
| --- | --- | --- |
| [Get Also](actions/get-also.md) | GET | Retrieves related phrases for a word from WordsAPI. |
| [Get Antonyms](actions/get-antonyms.md) | GET | Retrieves antonyms for a word from WordsAPI. |
| [Get Definitions](actions/get-definitions.md) | GET | Retrieves definitions for a word from WordsAPI. |
| [Get Entails](actions/get-entails.md) | GET | Retrieves implied words for a word from WordsAPI. |
| [Get Examples](actions/get-examples.md) | GET | Retrieves example sentences for a word from WordsAPI. |
| [Get Has Categories](actions/get-has-categories.md) | GET | Retrieves subcategories for a word from WordsAPI. |
| [Get Has Instances](actions/get-has-instances.md) | GET | Retrieves named instances of a word from WordsAPI. |
| [Get Has Members](actions/get-has-members.md) | GET | Retrieves group members for a word from WordsAPI. |
| [Get Has Parts](actions/get-has-parts.md) | GET | Retrieves component parts for a word from WordsAPI. |
| [Get Has Substances](actions/get-has-substances.md) | GET | Retrieves substances contained in a word from WordsAPI. |
| [Get Has Types](actions/get-has-types.md) | GET | Retrieves more specific terms for a word from WordsAPI. |
| [Get Has Usages](actions/get-has-usages.md) | GET | Retrieves domain examples for a word from WordsAPI. |
| [Get In Category](actions/get-in-category.md) | GET | Retrieves categories for a word from WordsAPI. |
| [Get In Region](actions/get-in-region.md) | GET | Retrieves regions where a word is used from WordsAPI. |
| [Get Instance Of](actions/get-instance-of.md) | GET | Retrieves broader classes for a word from WordsAPI. |
| [Get Member Of](actions/get-member-of.md) | GET | Retrieves groups that a word belongs to from WordsAPI. |
| [Get Part Of](actions/get-part-of.md) | GET | Retrieves larger wholes for a word from WordsAPI. |
| [Get Pertains To](actions/get-pertains-to.md) | GET | Retrieves related concepts for a word from WordsAPI. |
| [Get Random Word](actions/get-random-word.md) | GET | Retrieves a random word from WordsAPI. |
| [Get Region Of](actions/get-region-of.md) | GET | Retrieves words used in a region from WordsAPI. |
| [Get Rhymes](actions/get-rhymes.md) | GET | Retrieves rhyming words for a word from WordsAPI. |
| [Get Similar To](actions/get-similar-to.md) | GET | Retrieves similar words for a word from WordsAPI. |
| [Get Substance Of](actions/get-substance-of.md) | GET | Retrieves substances that a word is part of from WordsAPI. |
| [Get Synonyms](actions/get-synonyms.md) | GET | Retrieves synonyms for a word from WordsAPI. |
| [Get Type Of](actions/get-type-of.md) | GET | Retrieves broader terms for a word from WordsAPI. |
| [Get Usage Of](actions/get-usage-of.md) | GET | Retrieves usage domains for a word from WordsAPI. |
| [Get Word](actions/get-word.md) | GET | Retrieves full details for a word from WordsAPI. |

### Word Frequency

| Action | Method | Description |
| --- | --- | --- |
| [Get Frequency](actions/get-frequency.md) | GET | Retrieves frequency data for a word from WordsAPI. |

### Word Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Words](actions/search-words.md) | GET | Finds words in WordsAPI by search criteria. |

