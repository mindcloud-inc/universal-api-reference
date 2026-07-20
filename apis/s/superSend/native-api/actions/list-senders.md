# List Senders with SuperSend

Retrieves senders from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/senders`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Senders](https://docs.supersend.io/docs/sender)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TeamId` | query | `string` | no | — |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
| `search` | query | `string` | no | — |
| `provider` | query | `string` | no | — |
| `disabled` | query | `string` | no | Allowed values: true, false. |
| `warm` | query | `string` | no | Allowed values: true, false. |
