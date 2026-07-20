# Update Price with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/prices/:id`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Update Price](https://developer.surecart.com/api-reference/prices/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The price ID to update. |
| `price.name` | body | `string` | no | The updated display name for this price. |
