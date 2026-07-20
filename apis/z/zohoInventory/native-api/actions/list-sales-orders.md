# List Sales Orders with Zoho Inventory

Retrieves sales orders from Zoho Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/salesorders`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [List Sales Orders](https://www.zoho.com/inventory/api/v1/salesorders/#list-all-sales-orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
