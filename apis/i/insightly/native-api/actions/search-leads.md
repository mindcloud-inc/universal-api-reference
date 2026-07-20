# Search Leads with Insightly

Finds leads in Insightly by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Leads/Search`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Search Leads](https://api.insightly.com/v3.1/Help#!/Leads/GetEntitiesBySearch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_name` | query | `string` | no | Filter leads by this field name. |
| `field_value` | query | `string` | no | Filter leads by this field value. |
| `updated_after_utc` | query | `string` | no | Return leads updated after this UTC timestamp. |
| `brief` | query | `boolean` | no | Return only top-level properties for each lead. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
