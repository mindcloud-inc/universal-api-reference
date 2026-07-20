# Update Param Store with Statsig

Updates a param store in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/param_stores/{name}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Param Store](https://docs.statsig.com/api-reference/param-store/update-param-store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | — |
| `description` | body | `string` | no | Request body field. |
| `parameters` | body | `list` | no | Request body field. |
