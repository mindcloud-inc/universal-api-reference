# Create a Layer with Statsig

Creates a layer in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/layers`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create a Layer](https://docs.statsig.com/api-reference/layers/create-a-layer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `idType` | body | `string` | yes | Request body field. |
| `targetApps` | body | `string` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
