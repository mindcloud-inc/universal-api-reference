# List Projects with Insightly

Retrieves a list of projects from Insightly.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Projects`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [List Projects](https://api.insightly.com/v3.1/Help#!/Projects/GetEntities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brief` | query | `boolean` | no | Return only top-level properties for each project. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
