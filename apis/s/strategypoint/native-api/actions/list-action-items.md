# List Action Items with Strategypoint

Retrieves action items from Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/actionItems`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [List Action Items](https://developer.clearpointstrategy.com/reference/listactionitems-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of records to return. |
| `lastEdited` | query | `string` | no | Filter by last-edited timestamp. |
| `lastEditedBy` | query | `number` | no | Filter by the user who last edited the record. |
| `order` | query | `string` | no | Sort order for the result set. |
| `page` | query | `number` | no | Page number to return. |
