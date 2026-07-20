# Update customer record with WeForest

Updates an existing customer in WeForest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customers/:id`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Update customer record](https://docs.weforest.org/update-customer-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Customer identifier from WeForest. |
| `name` | body | `string` | yes | Updated customer name. |
