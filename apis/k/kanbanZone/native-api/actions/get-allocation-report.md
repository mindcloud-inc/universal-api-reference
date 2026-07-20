# Get Allocation Report with Kanban Zone

Retrieves an allocation report from Kanban Zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/board/:board/reports/allocation`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Get Allocation Report](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | path | `string` | yes | The board public ID. |
| `group_by` | query | `string` | yes | Group-by criteria: label, owner, column_state, or custom_field. |
| `custom_field` | query | `string` | no | Custom field label to use when Group By is custom_field |
| `include_cards` | query | `boolean` | no | Include card ID arrays in the response |
