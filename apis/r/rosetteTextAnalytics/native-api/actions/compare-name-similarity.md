# Compare Name Similarity with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/name-similarity`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Compare Name Similarity](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name1.text` | body | `string` | yes | First name text to compare. |
| `name1.language` | body | `string` | no | Three-letter ISO 639-3 language code for the first name. |
| `name1.entityType` | body | `string` | no | Entity type such as PERSON, LOCATION, ORGANIZATION, or IDENTIFIER. |
| `name2.text` | body | `string` | yes | Second name text to compare. |
| `name2.language` | body | `string` | no | Three-letter ISO 639-3 language code for the second name. |
| `name2.entityType` | body | `string` | no | Entity type such as PERSON, LOCATION, ORGANIZATION, or IDENTIFIER. |
