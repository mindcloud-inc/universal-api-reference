# Decode VIN Values with NHTSA vPIC

Retrieves flat decoded VIN values from NHTSA vPIC.

## Endpoint

- **Method:** `GET`
- **Path:** `vehicles/DecodeVinValues/:vin`
- **Base URL:** `https://vpic.nhtsa.dot.gov/api`
- **Official documentation:** [Decode VIN Values](https://vpic.nhtsa.dot.gov/api/Home/Index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelyear` | query | `string` | no | Optional model year to improve decoding accuracy for current or pre-1980 VINs. |
| `vin` | path | `string` | no | The VIN to decode. Partial VINs are also supported. |
| `vin` | path | `string` | yes | Vehicle Identification Number to decode in flat format. Partial VINs are supported with a * placeholder. |
| `modelyear` | query | `number` | no | Optional model year used to improve VIN decoding accuracy, especially for partial VINs. |
