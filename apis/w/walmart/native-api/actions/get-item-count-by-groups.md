# Get Item Count by Groups with Walmart

Retrieve the total number of items based on variant group information.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/items/groups/count`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Item Count by Groups](https://developer.walmart.com/us-marketplace/reference/getvariantcount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variantGroupId` | query | `string` | no | Retrieve all items with the same variant id |
