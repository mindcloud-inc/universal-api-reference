# List Item Activities with Teamhood

Retrieves Teamhood item activities for a board and time range.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards/:boardId/item-activities`
- **Base URL:** `https://api-mindcloud1.teamhood.com/api/v1`
- **Official documentation:** [List Item Activities](https://api-mindcloud1.teamhood.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | path | `string` | no | The Teamhood board ID. |
| `endDate` | body | `string` | no | The inclusive activity window end in ISO 8601 format. |
| `startDate` | body | `string` | no | The inclusive activity window start in ISO 8601 format. |
