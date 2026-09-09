# Get Item Count by Status with Walmart

Retrieve the total number of items filtered by a specific status.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/items/count`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Item Count by Status](https://developer.walmart.com/us-marketplace/reference/getvariantcount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | Status of Item  Allowed: `PUBLISHED`, `UNPUBLISHED`, `SYSTEM_PROBLEM`, `IN_PROGRESS`, `ALL` |
