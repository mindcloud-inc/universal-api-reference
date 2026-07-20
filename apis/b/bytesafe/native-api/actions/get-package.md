# Get Package with Bytesafe

Retrieves package details from a Bytesafe registry.

## Endpoint

- **Method:** `GET`
- **Path:** `/artifacts/registries/:registryName/packages/:packageName`
- **Base URL:** `https://mindcloud.bytesafe.dev/api/v1/`
- **Official documentation:** [Get Package](https://docs.bytesafe.dev/working-with-registries/internal-packages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageName` | path | `string` | yes | The package name to fetch. |
| `registryName` | path | `string` | yes | The registry name that contains the package. |
