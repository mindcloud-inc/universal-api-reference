# Query Series Data with Bureau of Labor Statistics

Finds Bureau of Labor Statistics data for one or more series.

## Endpoint

- **Method:** `POST`
- **Path:** `/timeseries/data/`
- **Base URL:** `https://api.bls.gov/publicAPI/v2`
- **Official documentation:** [Query Series Data](https://www.bls.gov/developers/api_signature_v2.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `seriesid` | body | `string<string>` | yes | One or more BLS series IDs. BLS expects the JSON key seriesid with an array of IDs. Send multiple values as a array. |
| `startyear` | body | `string` | no | Optional four-digit start year for the requested time frame. |
| `endyear` | body | `string` | no | Optional four-digit end year for the requested time frame. |
| `catalog` | body | `boolean` | no | Optional BLS flag to include catalog metadata when available. BLS registration may be required for enhanced optional fields. |
| `calculations` | body | `boolean` | no | Optional BLS flag to include available net and percent calculations. BLS registration may be required for enhanced optional fields. |
| `annualaverage` | body | `boolean` | no | Optional BLS flag to include annual averages when available. BLS registration may be required for enhanced optional fields. |
| `aspects` | body | `boolean` | no | Optional BLS flag to retrieve aspects associated with data points when available. BLS registration may be required for enhanced optional fields. |
