# Sync Datasource Documents with Tinq.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/datasources/sync/:workspaceId`
- **Base URL:** `https://tinq.ai`
- **Official documentation:** [Sync Datasource Documents](https://docs.tinq.ai/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasource` | body | `string` | yes | Datasource ID to sync. |
| `documents[]` | body | `array<string>` | no | Optional document slugs to sync; omit to let Tinq decide changed documents. |
