# Get region metadata with Zillow Econ

Retrieves region metadata from Zillow Econ.

## Endpoint

- **Method:** `GET`
- **Path:** `/zgecon/region`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get region metadata](https://bridgedataoutput.com/docs/explorer/zillow-group-econ-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stateCodeFIPS` | query | `string` | yes | Two-digit state FIPS code for the region metadata lookup. |
