# List Opportunities with Insightly

Retrieves a list of opportunities from Insightly.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Opportunities`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [List Opportunities](https://api.insightly.com/v3.1/Help#!/Opportunities/GetEntities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brief` | query | `boolean` | no | Return only top-level properties for each opportunity. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
