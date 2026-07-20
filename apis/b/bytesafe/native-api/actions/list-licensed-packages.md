# List Licensed Packages with Bytesafe

Retrieves licensed packages from a Bytesafe registry.

## Endpoint

- **Method:** `GET`
- **Path:** `/artifacts/registries/:registryName/licensed`
- **Base URL:** `https://mindcloud.bytesafe.dev/api/v1/`
- **Official documentation:** [List Licensed Packages](https://docs.bytesafe.dev/working-with-registries/package-licenses/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | License search query, for example MIT. |
| `registryName` | path | `string` | yes | The registry name to search for licensed packages. |
