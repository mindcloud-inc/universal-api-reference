# OEM VIN Lookup with Vincario

## Endpoint

- **Method:** `GET`
- **Path:** `/:apiKey/:controlSum/oem/:vin.:format`
- **Base URL:** `https://api.vincario.com/3.2`
- **Official documentation:** [OEM VIN Lookup](https://vincario.com/api-docs/3.2/#operations-OEM_VIN_Lookup-OEM_VIN_Lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vin` | path | `string` | yes | Vehicle Identification Number. |
