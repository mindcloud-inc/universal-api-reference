# VIN Decode with Vincario

## Endpoint

- **Method:** `GET`
- **Path:** `/:apiKey/:controlSum/decode/:vin.:format`
- **Base URL:** `https://api.vincario.com/3.2`
- **Official documentation:** [VIN Decode](https://vincario.com/api-docs/3.2/#operations-VIN_Decode-VIN_Decode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vin` | path | `string` | yes | Vehicle Identification Number. |
