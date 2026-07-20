# Search Projects with Insightly

Finds projects in Insightly by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Projects/Search`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Search Projects](https://api.insightly.com/v3.1/Help#!/Projects/GetEntitiesBySearch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_name` | query | `string` | no | Filter projects by this field name. |
| `field_value` | query | `string` | no | Filter projects by this field value. |
| `updated_after_utc` | query | `string` | no | Return projects updated after this UTC timestamp. |
| `brief` | query | `boolean` | no | Return only top-level properties for each project. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
