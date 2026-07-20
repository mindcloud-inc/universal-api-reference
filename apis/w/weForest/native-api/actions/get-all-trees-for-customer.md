# Get all trees for customer with WeForest

Retrieves all trees for a customer in WeForest.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:id/trees`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Get all trees for customer](https://docs.weforest.org/get-all-trees-for-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Customer identifier from WeForest. |
| `count` | query | `boolean` | no | Fetch the total count of all order quantities. |
| `startDate` | query | `string` | no | Start of date range for order requests in YYYY-MM-DD format. |
| `endDate` | query | `string` | no | End of date range for order requests in YYYY-MM-DD format. |
