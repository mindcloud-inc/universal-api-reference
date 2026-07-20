# Get market report with Zillow Econ

Retrieves market report data from Zillow Econ.

## Endpoint

- **Method:** `GET`
- **Path:** `/zgecon/marketreport`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get market report](https://bridgedataoutput.com/docs/explorer/zillow-group-econ-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stateCodeFIPS` | query | `string` | yes | Two-digit state FIPS code for the market report region. |
