# List Financial Institutions with Column

## Endpoint

- **Method:** `GET`
- **Path:** `/institutions`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [List Financial Institutions](https://column.com/docs/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | ISO 3166-1 Alpha-2 country code for institution filtering. |
| `name` | query | `string` | no | Case-insensitive keywords in institution full names. |
| `routing_number_type` | query | `string` | no | Routing number type filter: aba or bic. |
