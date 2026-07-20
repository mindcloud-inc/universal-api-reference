# List Audiences with CDC Content Services

Retrieves audiences from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/audiences`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Audiences](https://tools.cdc.gov/api/docs/info.aspx)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `string` | no | Language filter; CDC defaults to English when omitted. |
