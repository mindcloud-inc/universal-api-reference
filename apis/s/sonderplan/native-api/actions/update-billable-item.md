# Update Billable Item with Sonderplan

## Endpoint

- **Method:** `PUT`
- **Path:** `/billable-item`
- **Base URL:** `https://api.sonderplan.com/v2`
- **Official documentation:** [Update Billable Item](https://docs.sonderplan.com/api-reference/billable-item/update-billable-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Billable item payload. |
| `id` | query | `string` | yes | Billable item ID. |
