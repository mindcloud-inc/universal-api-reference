# List Leads with Insightly

Retrieves a list of leads from Insightly.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Leads`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [List Leads](https://api.insightly.com/v3.1/Help#!/Leads/GetEntities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brief` | query | `boolean` | no | Return only top-level properties for each lead. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
