# Get Word Suggestions with Datamuse

Retrieves Datamuse word suggestions for partial search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/sug`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Get Word Suggestions](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | yes | Partial text entered by the user for autocomplete suggestions. |
