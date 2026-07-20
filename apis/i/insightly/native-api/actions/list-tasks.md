# List Tasks with Insightly

Retrieves a list of tasks from Insightly.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Tasks`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [List Tasks](https://api.insightly.com/v3.1/Help#!/Tasks/GetEntities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brief` | query | `boolean` | no | Return only top-level properties for each task. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
