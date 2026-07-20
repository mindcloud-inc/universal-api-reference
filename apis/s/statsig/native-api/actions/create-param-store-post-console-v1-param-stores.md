# Create Param Store with Statsig

Creates a param store in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/param_stores`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Param Store](https://docs.statsig.com/api-reference/param-store/create-param-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | yes | Request body field. |
| `displayName` | body | `string` | yes | Request body field. |
| `targetAppIDs` | body | `list` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
