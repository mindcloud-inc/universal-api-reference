# List Popular Series with Bureau of Labor Statistics

Retrieves popular Bureau of Labor Statistics series IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeseries/popular`
- **Base URL:** `https://api.bls.gov/publicAPI/v2`
- **Official documentation:** [List Popular Series](https://www.bls.gov/developers/api_signature_v2.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey` | query | `string` | no | Optional BLS survey abbreviation, for example LA, to return popular series for one survey. |
