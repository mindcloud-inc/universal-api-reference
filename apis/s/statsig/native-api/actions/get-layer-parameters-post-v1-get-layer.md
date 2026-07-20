# Get Layer Parameters with Statsig

Retrieves layer parameters from Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/get_layer`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get Layer Parameters](https://docs.statsig.com/api-reference/layers/get-layer-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layerName` | body | `string` | yes | Name of the layer. |
| `user` | body | `object` | yes | Statsig user object containing at least one identifier. |
| `statsigMetadata` | body | `object` | no | SDK metadata for diagnostics and exposure behavior. |
