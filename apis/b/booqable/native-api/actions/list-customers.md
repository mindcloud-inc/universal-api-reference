# List Customers with Booqable

Retrieves customer records from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [List Customers](https://developers.booqable.com/#customers-list-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[customers]` | query | `string` | no | Comma-separated customer fields to include instead of the default field set. |
| `filter` | query | `object` | no | Field-qualified customer filters using Booqable filter syntax. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
