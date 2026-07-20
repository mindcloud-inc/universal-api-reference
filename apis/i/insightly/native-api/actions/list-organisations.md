# List Organisations with Insightly

Retrieves a list of organisations from Insightly.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Organisations`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [List Organisations](https://api.insightly.com/v3.1/Help#!/Organisations/GetEntities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brief` | query | `boolean` | no | Return only top-level properties for each organisation. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
