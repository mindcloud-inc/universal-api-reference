# List Goals with Strategypoint

Retrieves goals from Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/goals`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [List Goals](https://developer.clearpointstrategy.com/reference/listgoals-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of records to return. |
| `lastEdited` | query | `string` | no | Filter by last-edited timestamp. |
| `lastEditedBy` | query | `number` | no | Filter by the user who last edited the record. |
| `order` | query | `string` | no | Sort order for the result set. |
| `page` | query | `number` | no | Page number to return. |
