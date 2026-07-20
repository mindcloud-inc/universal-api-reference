# List Logs for Subscription Following with Vybit

## Endpoint

- **Method:** `GET`
- **Path:** `/logs/subscription/following/{{followingKey}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [List Logs for Subscription Following](https://developer.vybit.net/api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `followingKey` | path | `string` | yes | The unique following key of the subscription whose logs to list. |
| `limit` | query | `number` | no | Maximum number of log records to return. |
| `offset` | query | `number` | no | Number of log records to skip. |
| `search` | query | `string` | no | Search logs by vybit name or diagnostic fields. |
