# Get Bot with Recallai

Retrieves a bot from Recallai.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/bot/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Get Bot](https://docs.recall.ai/reference/bot_retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this bot. |
