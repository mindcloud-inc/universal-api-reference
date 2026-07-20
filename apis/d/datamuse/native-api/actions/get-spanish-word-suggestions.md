# Get Spanish Word Suggestions with Datamuse

Retrieves Spanish word suggestions from Datamuse for partial search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/sug`
- **Base URL:** `https://api.datamuse.com`
- **Official documentation:** [Get Spanish Word Suggestions](https://www.datamuse.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | yes | Partial Spanish text entered by the user for autocomplete suggestions. |
