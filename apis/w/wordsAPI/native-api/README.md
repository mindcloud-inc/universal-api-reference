# WordsAPI: Native API Reference

A consolidated summary of WordsAPI's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://www.wordsapi.com/docs/
- **API base URL:** `https://wordsapiv1.p.rapidapi.com`

## Authentication

### RapidAPI Key

Authenticate WordsAPI requests with a RapidAPI application key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-RapidAPI-Key: <apiKey>
```

[Official authentication documentation](https://www.wordsapi.com/docs/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Also](actions/get-also.md) | `GET /words/{word}/also` | [docs](https://www.wordsapi.com/docs/) |
| [Get Antonyms](actions/get-antonyms.md) | `GET /words/{word}/antonyms` | [docs](https://www.wordsapi.com/docs/) |
| [Get Definitions](actions/get-definitions.md) | `GET /words/{word}/definitions` | [docs](https://www.wordsapi.com/docs/) |
| [Get Entails](actions/get-entails.md) | `GET /words/{word}/entails` | [docs](https://www.wordsapi.com/docs/) |
| [Get Examples](actions/get-examples.md) | `GET /words/{word}/examples` | [docs](https://www.wordsapi.com/docs/) |
| [Get Frequency](actions/get-frequency.md) | `GET /words/{word}/frequency` | [docs](https://www.wordsapi.com/docs/) |
| [Get Has Categories](actions/get-has-categories.md) | `GET /words/{word}/hasCategories` | [docs](https://www.wordsapi.com/docs/) |
| [Get Has Instances](actions/get-has-instances.md) | `GET /words/{word}/hasInstances` | [docs](https://www.wordsapi.com/docs/) |
| [Get Has Members](actions/get-has-members.md) | `GET /words/{word}/hasMembers` | [docs](https://www.wordsapi.com/docs/) |
| [Get Has Parts](actions/get-has-parts.md) | `GET /words/{word}/hasParts` | [docs](https://www.wordsapi.com/docs/) |
| [Get Has Substances](actions/get-has-substances.md) | `GET /words/{word}/hasSubstances` | [docs](https://www.wordsapi.com/docs/) |
| [Get Has Types](actions/get-has-types.md) | `GET /words/{word}/hasTypes` | [docs](https://www.wordsapi.com/docs/) |
| [Get Has Usages](actions/get-has-usages.md) | `GET /words/{word}/hasUsages` | [docs](https://www.wordsapi.com/docs/) |
| [Get In Category](actions/get-in-category.md) | `GET /words/{word}/inCategory` | [docs](https://www.wordsapi.com/docs/) |
| [Get In Region](actions/get-in-region.md) | `GET /words/{word}/inRegion` | [docs](https://www.wordsapi.com/docs/) |
| [Get Instance Of](actions/get-instance-of.md) | `GET /words/{word}/instanceOf` | [docs](https://www.wordsapi.com/docs/) |
| [Get Member Of](actions/get-member-of.md) | `GET /words/{word}/memberOf` | [docs](https://www.wordsapi.com/docs/) |
| [Get Part Of](actions/get-part-of.md) | `GET /words/{word}/partOf` | [docs](https://www.wordsapi.com/docs/) |
| [Get Pertains To](actions/get-pertains-to.md) | `GET /words/{word}/pertainsTo` | [docs](https://www.wordsapi.com/docs/) |
| [Get Random Word](actions/get-random-word.md) | `GET /words` | [docs](https://www.wordsapi.com/docs/) |
| [Get Region Of](actions/get-region-of.md) | `GET /words/{word}/regionOf` | [docs](https://www.wordsapi.com/docs/) |
| [Get Rhymes](actions/get-rhymes.md) | `GET /words/{word}/rhymes` | [docs](https://www.wordsapi.com/docs/) |
| [Get Similar To](actions/get-similar-to.md) | `GET /words/{word}/similarTo` | [docs](https://www.wordsapi.com/docs/) |
| [Get Substance Of](actions/get-substance-of.md) | `GET /words/{word}/substanceOf` | [docs](https://www.wordsapi.com/docs/) |
| [Get Synonyms](actions/get-synonyms.md) | `GET /words/{word}/synonyms` | [docs](https://www.wordsapi.com/docs/) |
| [Get Type Of](actions/get-type-of.md) | `GET /words/{word}/typeOf` | [docs](https://www.wordsapi.com/docs/) |
| [Get Usage Of](actions/get-usage-of.md) | `GET /words/{word}/usageOf` | [docs](https://www.wordsapi.com/docs/) |
| [Get Word](actions/get-word.md) | `GET /words/{word}` | [docs](https://www.wordsapi.com/docs/) |
| [Search Words](actions/search-words.md) | `GET /words` | [docs](https://www.wordsapi.com/docs/) |
