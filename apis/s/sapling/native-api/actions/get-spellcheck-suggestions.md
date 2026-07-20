# Get Spellcheck Suggestions with Sapling

Retrieves spellcheck suggestions for text from Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/spellcheck`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Get Spellcheck Suggestions](https://sapling.ai/docs/api/spellcheck/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to check for spelling errors. |
| `session_id` | body | `string` | no | Optional document or session identifier for the spellcheck request. |
