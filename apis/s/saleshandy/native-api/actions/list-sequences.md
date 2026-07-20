# List Sequences with Saleshandy

## Endpoint

- **Method:** `GET`
- **Path:** `/sequences`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [List Sequences](https://developer.saleshandy.com/api-reference/sequences/list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sequenceName` | query | `string` | no | Search by sequence title. |
| `clientIds` | query | `string` | no | Filter sequences by client IDs. |
