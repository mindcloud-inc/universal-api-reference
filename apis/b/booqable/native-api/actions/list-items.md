# List Items with Booqable

Retrieves item records from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/items`
- **Base URL:** `https://{companySlug}.booqable.com/api/4`
- **Official documentation:** [List Items](https://developers.booqable.com/#items-list-items)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[items]` | query | `string` | no | Comma-separated item fields to include instead of the default field set. |
| `filter` | query | `string` | no | Booqable filters as a JSON object, for example {"archived":{"eq":false}}. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
| `meta` | query | `string` | no | Booqable metadata as a JSON object, for example {"total":["count"]}. |
