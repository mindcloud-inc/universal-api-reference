# Create Key with Statsig

Creates a key in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/keys`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Key](https://docs.statsig.com/api-reference/keys/create-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Request body field. |
| `type` | body | `string` | yes | Request body field. |
| `scopes` | body | `list` | no | Request body field. |
| `environments` | body | `list` | no | Request body field. |
| `targetAppID` | body | `string` | no | Request body field. |
| `secondaryTargetAppIDs` | body | `list` | no | Request body field. |
