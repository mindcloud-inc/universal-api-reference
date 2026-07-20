# Get Abandoned Effort Report with Kanban Zone

Retrieves an abandoned effort report from Kanban Zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/board/:board/reports/abandoned-effort`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Get Abandoned Effort Report](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | path | `string` | yes | The board public ID. |
| `start` | query | `date` | yes | Start of the time window in ISO 8601 format. |
| `end` | query | `date` | yes | End of the time window in ISO 8601 format. |
| `include_cards` | query | `boolean` | no | Include card ID arrays in the response |
