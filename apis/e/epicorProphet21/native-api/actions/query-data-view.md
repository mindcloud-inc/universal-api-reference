# Query Data View with Epicor Prophet 21

## Endpoint

- **Method:** `GET`
- **Path:** `/data/erp/views/v1/:view`
- **Base URL:** `{apiUrl}`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view` | path | `string` | no | The Prophet 21 data view name, such as p21_view_customer. |
| `$select` | query | `string` | no | Comma-separated field names. Leave empty to return all available fields. |
| `$filter` | query | `string` | no | A Prophet 21 filter expression, such as customer_id eq 123. |
| `$count` | query | `boolean` | no | Format: `toggle`. |
