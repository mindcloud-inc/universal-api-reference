# List Logs for Owned Vybit with Vybit

## Endpoint

- **Method:** `GET`
- **Path:** `/logs/vybit/{{vybKey}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [List Logs for Owned Vybit](https://developer.vybit.net/api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of log records to return. |
| `offset` | query | `number` | no | Number of log records to skip. |
| `search` | query | `string` | no | Search logs by vybit name or diagnostic fields. |
| `vybKey` | path | `string` | yes | The unique key of the owned vybit whose logs to list. |
