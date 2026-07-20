# Search Organisations with Insightly

Finds organisations in Insightly by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Organisations/Search`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Search Organisations](https://api.insightly.com/v3.1/Help#!/Organisations/GetEntitiesBySearch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_name` | query | `string` | no | Filter organisations by this field name. |
| `field_value` | query | `string` | no | Filter organisations by this field value. |
| `updated_after_utc` | query | `string` | no | Return organisations updated after this UTC timestamp. |
| `brief` | query | `boolean` | no | Return only top-level properties for each organisation. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
