# Get Latest Carbon Intensity with Electricity Maps

## Endpoint

- **Method:** `GET`
- **Path:** `/carbon-intensity/latest`
- **Base URL:** `https://api.electricitymaps.com/v4`
- **Official documentation:** [Get Latest Carbon Intensity](https://app.electricitymaps.com/developer-hub/api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `disableEstimations` | query | `boolean` | no | When true, only measured data is returned. |
| `emissionFactorType` | query | `list` | no | Choose lifecycle or direct emission factors. Accepted values: `0`, `1`. |
| `temporalGranularity` | query | `list` | no | Requested time granularity. Accepted values: `0`, `1`, `2`. |
| `zone` | query | `string` | yes | Zone key to query, for example BR-S. |
