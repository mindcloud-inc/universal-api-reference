# Delete Documents with Tinq.ai

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/documents/delete`
- **Base URL:** `https://tinq.ai`
- **Official documentation:** [Delete Documents](https://docs.tinq.ai/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documents[]` | body | `array<string>` | yes | One or more document slugs to delete. |
