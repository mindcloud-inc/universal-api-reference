# Accept Completion with Sapling

Records an accepted autocomplete completion in Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/complete/:completionId/accept`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Accept Completion](https://sapling.ai/docs/api/autocomplete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `completionId` | path | `string` | yes | Completion UUID returned from autocomplete. |
| `context.query` | body | `string` | yes | The original query used to generate the completion. |
| `context.completion` | body | `string` | yes | The accepted completion string. |
| `session_id` | body | `string` | no | Document or session identifier. |
