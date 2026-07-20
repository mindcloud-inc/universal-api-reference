# Get Word Entries with Free Dictionary

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/entries/:language/:word`
- **Base URL:** `https://api.dictionaryapi.dev`
- **Official documentation:** [Get Word Entries](https://dictionaryapi.dev/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | path | `string` | yes | Supported language code for the dictionary lookup. Upstream source supports hi, en, en_GB, en_US, es, fr, ja, cs, nl, sk, ru, de, it, ko, pt-BR, ar, and tr. |
| `word` | path | `string` | yes | The English word to look up. |
| `include` | query | `string` | no | Optional comma-separated expansions. Use `example` to include full examples arrays in the response where available. |
