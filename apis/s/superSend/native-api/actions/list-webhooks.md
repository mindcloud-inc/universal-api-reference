# List Webhooks with SuperSend

Retrieves webhooks from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Webhooks](https://docs.supersend.io/docs/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | query | `string` | yes | — |
| `enabled` | query | `boolean` | no | — |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
