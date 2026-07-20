# Get Item By UUID with Rollbar

Retrieves an item from Rollbar by occurrence UUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Item By UUID](https://docs.rollbar.com/reference/get-an-item-by-occurrence-uuid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | query | `string` | yes | Occurrence UUID for the target item |
