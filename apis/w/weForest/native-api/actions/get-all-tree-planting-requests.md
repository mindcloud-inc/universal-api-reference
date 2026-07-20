# Get all tree-planting requests with WeForest

Retrieves all tree-planting requests from WeForest.

## Endpoint

- **Method:** `GET`
- **Path:** `/trees`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Get all tree-planting requests](https://docs.weforest.org/get-all-tree-planting-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `boolean` | no | Fetch the total count of all order quantities. |
| `endDate` | query | `string` | no | End of date range for order requests in YYYY-MM-DD format. |
| `startDate` | query | `string` | no | Start of date range for order requests in YYYY-MM-DD format. |
