# List Estimates with SOS Inventory

Retrieves estimates from SOS Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/estimate`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Estimates](https://developer.sosinventory.com/apidoc/Estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `string` | no | Return archived yes/no estimates. |
| `channel` | query | `string` | no | Filter by channel name. |
| `query` | query | `string` | no | Filter by number, comment, or customer name. |
| `status` | query | `string` | no | Filter by accepted, pending, closed, or rejected status. |
