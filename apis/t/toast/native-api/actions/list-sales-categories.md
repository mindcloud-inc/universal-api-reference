# List Sales Categories with Toast

Retrieves menu-item sales categories configured for the connected restaurant.

## Endpoint

- **Method:** `GET`
- **Path:** `/config/v2/salesCategories`
- **Base URL:** `{connection}`
- **API:** Configuration
- **Official documentation:** [List Sales Categories](https://doc.toasttab.com/openapi/configuration/operation/salesCategoriesGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastModified` | query | `date` | no | Return objects created or modified after this date and time. |
