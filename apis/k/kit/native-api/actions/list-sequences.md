# List Sequences with Kit

Lists sequences in your Kit account.

## Endpoint

- **Method:** `GET`
- **Path:** `/sequences`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Sequences](https://developers.kit.com/api-reference/sequences/list-sequences)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return results after this cursor. |
| `before` | query | `string` | no | Return results before this cursor. |
| `include_total_count` | query | `boolean` | no | Include total_count in pagination metadata. |
| `per_page` | query | `number` | no | Number of results per page. |
