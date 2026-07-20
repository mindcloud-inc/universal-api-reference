# List Quarantined Packages with Bytesafe

Retrieves quarantined packages from a Bytesafe registry.

## Endpoint

- **Method:** `GET`
- **Path:** `/artifacts/registries/:registryName/quarantined`
- **Base URL:** `https://mindcloud.bytesafe.dev/api/v1/`
- **Official documentation:** [List Quarantined Packages](https://docs.bytesafe.dev/quarantine/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registryName` | path | `string` | yes | The registry name that contains quarantined packages. |
