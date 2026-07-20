# List Item Occurrences with Rollbar

Retrieves item occurrences from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:itemId/instances`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List Item Occurrences](https://docs.rollbar.com/reference/get_api-1-item-item-id-instances)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `number` | yes | Rollbar item identifier. |
