# Search Customers with Booqable

Finds customers in Booqable by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/search`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Search Customers](https://developers.booqable.com/#customers-search-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[customers]` | body | `string` | no | Comma-separated customer fields to include instead of the default field set. |
| `filter` | body | `object` | no | Advanced customer search filter object using Booqable's logical conditions syntax. |
| `include` | body | `string` | no | Comma-separated relationships to sideload. |
