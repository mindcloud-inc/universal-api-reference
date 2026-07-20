# List Items with Booqable

Retrieves item records from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/items`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [List Items](https://developers.booqable.com/#items-list-items)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[items]` | query | `string` | no | Comma-separated item fields to include instead of the default field set. |
| `filter` | query | `object` | no | Provider-specific item filters. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
| `meta` | query | `object` | no | Metadata aggregations to request from Booqable. |
