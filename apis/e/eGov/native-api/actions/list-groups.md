# List Groups with e-Gov

Retrieves groups from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/group_list`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [List Groups](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `all_fields` | query | `boolean` | no | Return full group records instead of names. |
| `include_dataset_count` | query | `boolean` | no | — |
| `include_extras` | query | `boolean` | no | — |
| `include_tags` | query | `boolean` | no | — |
| `include_groups` | query | `boolean` | no | — |
| `include_users` | query | `boolean` | no | — |
| `sort` | query | `string` | no | — |
| `order_by` | query | `string` | no | — |
