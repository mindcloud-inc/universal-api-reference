# Get Autocomplete with Sapling

Retrieves autocomplete suggestions for text from Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/complete`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Get Autocomplete](https://sapling.ai/docs/api/autocomplete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Text that should be autocompleted. |
| `session_id` | body | `string` | no | Document or session identifier. |
