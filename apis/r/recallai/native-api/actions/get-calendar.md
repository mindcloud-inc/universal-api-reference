# Get Calendar with Recallai

Retrieves a calendar from Recallai.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/calendars/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Get Calendar](https://docs.recall.ai/reference/calendars_retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this calendar. |
