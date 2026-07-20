# List Users with Strategypoint

Retrieves users from Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [List Users](https://developer.clearpointstrategy.com/reference/listusers-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of records to return. |
| `email` | query | `string` | no | Filter users by email address. |
| `lastEdited` | query | `string` | no | Filter by last-edited timestamp. |
| `lastEditedBy` | query | `number` | no | Filter by the user who last edited the record. |
| `order` | query | `string` | no | Sort order for the result set. |
| `page` | query | `number` | no | Page number to return. |
