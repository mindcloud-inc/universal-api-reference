# Get Flow Efficiency Report with Kanban Zone

Retrieves a flow efficiency report from Kanban Zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/board/:board/reports/flow-efficiency`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Get Flow Efficiency Report](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | path | `string` | yes | The board public ID. |
| `start` | query | `date` | yes | Start of the time window in ISO 8601 format. |
| `end` | query | `date` | yes | End of the time window in ISO 8601 format. |
| `include_cards` | query | `boolean` | no | Include card ID arrays in the response |
