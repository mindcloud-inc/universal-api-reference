# Update a layer with Statsig

Updates a layer in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/layers/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update a layer](https://docs.statsig.com/api-reference/layers/update-a-layer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `description` | body | `string` | yes | Request body field. |
| `parameters` | body | `list` | yes | Request body field. |
| `targetApps` | body | `string` | no | Request body field. |
