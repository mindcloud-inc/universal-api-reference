# Compare Entities with Tisane Labs

Compares named entities in Tisane Labs.

## Endpoint

- **Method:** `POST`
- **Path:** `/compare/entities`
- **Base URL:** `https://api.tisane.ai`
- **Official documentation:** [Compare Entities](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/compareEntities)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language1` | body | `string` | yes | IETF language tag for the first entity. |
| `entity1` | body | `string` | yes | First compound named entity to compare. |
| `language2` | body | `string` | yes | IETF language tag for the second entity. |
| `entity2` | body | `string` | yes | Second compound named entity to compare. |
