# List Teams with SuperSend

Retrieves teams from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Teams](https://docs.supersend.io/docs/team)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
| `search` | query | `string` | no | Search teams by name. |
| `all` | query | `string` | no | List all org teams (admin only) Allowed values: true, false. |
