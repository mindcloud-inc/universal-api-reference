# List Orders with Booqable

Retrieves order records from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [List Orders](https://developers.booqable.com/#orders-list-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[orders]` | query | `string` | no | Comma-separated order fields to include instead of the default fields. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
| `filter` | query | `object` | no | Raw filter object using Booqable filter[field][operator]=value semantics. |
| `meta[total][]` | query | `array<string>` | no | Aggregations to include in meta.total. |
