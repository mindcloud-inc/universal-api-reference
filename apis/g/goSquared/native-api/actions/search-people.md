# Search People with GoSquared

Finds people in GoSquared by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `people/v1/people`
- **Base URL:** `https://api.gosquared.com`
- **Official documentation:** [Search People](https://www.gosquared.com/docs/people/people/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | The search term to match against People records. |
| `fields` | query | `string` | no | A comma-delimited list of fields to include in each result row. |
| `presenter` | query | `string` | no | Modifies the response data structure. |
| `dateFormat` | query | `string` | no | Moment-compatible format for returned date values. |
