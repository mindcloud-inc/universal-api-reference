# Search Customer Organizations With Details with OneDesk

Finds customer organizations in OneDesk by filters, with details.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/public/customer-organizations/filter/details`
- **Base URL:** `https://app.onedesk.com`
- **Official documentation:** [Search Customer Organizations With Details](https://onedesk.com/public-api/swagger.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties[]` | body | `array<object>` | no | Array of OneDesk property filters. |
| `properties[].operation` | body | `string` | no | Comparison operation to apply to the property. |
| `properties[].property` | body | `string` | no | Name of property to be filtered. |
| `properties[].value` | body | `string` | no | Value used in the filter comparison. |
| `limit` | body | `number` | no | Maximum number of customer organization detail rows to return. |
