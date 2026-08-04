# List Menu Items with Toast

Retrieves menu items and modifiers configured for the connected restaurant.

## Endpoint

- **Method:** `GET`
- **Path:** `/config/v2/menuItems`
- **Base URL:** `{connection}`
- **API:** Configuration
- **Official documentation:** [List Menu Items](https://doc.toasttab.com/openapi/configuration/operation/menuItemsGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastModified` | query | `date` | no | Return objects created or modified after this date and time. |
