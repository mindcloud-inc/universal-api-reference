# Search Contacts with Insightly

Finds contacts in Insightly by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Contacts/Search`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Search Contacts](https://api.insightly.com/v3.1/Help#!/Contacts/GetEntitiesBySearch)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_name` | query | `string` | no | Filter contacts by this field name. |
| `field_value` | query | `string` | no | Filter contacts by this field value. |
| `updated_after_utc` | query | `string` | no | Return contacts updated after this UTC timestamp. |
| `brief` | query | `boolean` | no | Return only top-level properties for each contact. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
