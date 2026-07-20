# List listings with Zillow MLS Data

Retrieves listings from a Zillow MLS Data dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/listings`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [List listings](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code to read listings from. |
