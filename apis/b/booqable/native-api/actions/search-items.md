# Search Items with Booqable

Finds items in Booqable by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/items/search`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Search Items](https://developers.booqable.com/#items-search-items)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[items]` | body | `string` | no | Comma-separated item fields to include instead of the default field set. |
| `filter` | body | `object` | no | Provider-specific item filters, including advanced `conditions` groups. |
| `include` | body | `string` | no | Comma-separated relationships to sideload. |
| `meta` | body | `object` | no | Metadata aggregations to request from Booqable. |
