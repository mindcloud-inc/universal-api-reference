# Get Edits with Sapling

Retrieves grammar edits for text from Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/edits`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Get Edits](https://sapling.ai/docs/api/edits-overview/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to process for grammar, spelling, and stylistic edits. |
| `session_id` | body | `string` | no | Optional document or session identifier for the text being checked. |
