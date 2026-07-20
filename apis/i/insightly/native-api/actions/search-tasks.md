# Search Tasks with Insightly

Finds tasks in Insightly by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Tasks/Search`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Search Tasks](https://api.insightly.com/v3.1/Help#!/Tasks/GetEntitiesBySearch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_name` | query | `string` | no | Filter tasks by this field name. |
| `field_value` | query | `string` | no | Filter tasks by this field value. |
| `updated_after_utc` | query | `string` | no | Return tasks updated after this UTC timestamp. |
| `brief` | query | `boolean` | no | Return only top-level properties for each task. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
