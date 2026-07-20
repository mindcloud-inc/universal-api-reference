# Get License with Bytesafe

Retrieves package license details from Bytesafe.

## Endpoint

- **Method:** `GET`
- **Path:** `/licenses/:licenseKey`
- **Base URL:** `https://mindcloud.bytesafe.dev/api/v1/`
- **Official documentation:** [Get License](https://docs.bytesafe.dev/working-with-registries/package-licenses/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licenseKey` | path | `string` | yes | The SPDX or Bytesafe license key. |
