# Export Version Data with Openlayer

Exports version data from the Openlayer API.

## Endpoint

- **Method:** `POST`
- **Path:** `/versions/:versionId/export`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Export Version Data](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fmt` | body | `string` | yes | Export format. |
| `label` | query | `string` | yes | Optional export label. |
| `versionId` | path | `string` | yes | The project version ID. |
