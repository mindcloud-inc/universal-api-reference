# Partially update a layer with Statsig

Updates a layer in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/layers/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Partially update a layer](https://docs.statsig.com/api-reference/layers/partially-update-a-layer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `description` | body | `string` | no | Request body field. |
| `parameters` | body | `list` | no | Request body field. |
| `targetApps` | body | `string` | no | Request body field. |
