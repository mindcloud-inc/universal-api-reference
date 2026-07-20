# Get Package with Zoho Inventory

Retrieves a package from Zoho Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/packages/:package_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Get Package](https://www.zoho.com/inventory/api/v1/packages/#retrieving-a-package)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `package_id` | path | `string` | yes | The Zoho Inventory package_id for the package. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
