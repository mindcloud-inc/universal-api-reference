# Get Registry Graph with Bytesafe

Retrieves a registry graph from Bytesafe dashboards.

## Endpoint

- **Method:** `GET`
- **Path:** `/artifacts/registries/:registryName/graph`
- **Base URL:** `https://mindcloud.bytesafe.dev/api/v1/`
- **Official documentation:** [Get Registry Graph](https://docs.bytesafe.dev/working-with-registries/dashboards/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registryName` | path | `string` | yes | The Bytesafe registry name to inspect. |
