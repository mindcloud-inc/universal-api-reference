# Get office with Zillow MLS Data

Retrieves a specific office from Zillow MLS Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/offices/:officeId`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get office](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code that contains the office. |
| `officeId` | path | `string` | yes | Office identifier from the Bridge dataset. |
