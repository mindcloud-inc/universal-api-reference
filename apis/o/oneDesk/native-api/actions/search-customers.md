# Search Customers with OneDesk

Finds customers in OneDesk by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/public/customers/filter`
- **Base URL:** `https://app.onedesk.com`
- **Official documentation:** [Search Customers](https://onedesk.com/public-api/swagger.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties[]` | body | `array<object>` | no | Array of OneDesk property filters. |
| `properties[].operation` | body | `string` | no | Comparison operation to apply to the property. |
| `properties[].property` | body | `string` | no | Name of property to be filtered. |
| `properties[].value` | body | `string` | no | Value used in the filter comparison. |
| `limit` | body | `number` | no | Maximum number of customers to return. |
