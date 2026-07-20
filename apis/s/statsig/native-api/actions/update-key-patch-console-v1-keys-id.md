# Update Key with Statsig

Updates a key in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/keys/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Key](https://docs.statsig.com/api-reference/keys/update-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `description` | body | `string` | no | Request body field. |
| `scopes` | body | `list` | no | Request body field. |
| `environments` | body | `list` | no | Request body field. |
| `targetAppID` | body | `string` | no | Request body field. |
| `secondaryTargetAppIDs` | body | `list` | no | Request body field. |
