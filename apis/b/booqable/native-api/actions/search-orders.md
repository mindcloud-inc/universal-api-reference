# Search Orders with Booqable

Finds orders in Booqable by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/search`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Search Orders](https://developers.booqable.com/#orders-search-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[orders]` | body | `string` | no | Comma-separated order fields to include instead of the default fields. |
| `include` | body | `string` | no | Comma-separated relationships to sideload. |
| `filter` | body | `object` | no | Search filter object using direct field filters, for example `filter.status.eq = draft`. In runtime testing, the grouped `conditions` shape returned a provider validation error. |
| `meta[total][]` | body | `array<string>` | no | Aggregations to include in meta.total. |
