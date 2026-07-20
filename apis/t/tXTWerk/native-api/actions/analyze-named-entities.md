# Analyze Named Entities with TXT Werk

Retrieves named entities from text in TXT Werk.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/txt/analyzer`
- **Base URL:** `https://api.txtwerk.de`
- **Official documentation:** [Analyze Named Entities](https://services.txtwerk.de/ws/documentation/showRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to analyze. |
| `language` | body | `string` | no | Optional input language; omit to let TXT Werk detect it automatically. |
| `nentities` | body | `number` | no | Maximum number of entities to return. |
| `nerMinConfidence` | body | `number` | no | Minimum confidence threshold for returned entities. |
| `nerMinRelevance` | body | `number` | no | Minimum relevance threshold for returned entities. |
