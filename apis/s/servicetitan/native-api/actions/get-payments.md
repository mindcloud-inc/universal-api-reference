# Get Payments with ServiceTitan

Gets a paginated list of payments

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/payments`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Payments](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Payments_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `statuses` | query | `string` | no | — |
| `totalLess` | query | `number` | no | — |
| `totalGreater` | query | `number` | no | — |
| `ids` | query | `string` | no | — |
| `createdBefore` | query | `string` | no | Return items created before certain date/time (in UTC) |
| `createdOnOrAfter` | query | `string` | no | Return items created on or after certain date/time (in UTC) |
| `sort` | query | `string` | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order. |
