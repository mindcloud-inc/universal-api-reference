# List assessments with Zillow Public Records

Retrieves public property assessments from Zillow Public Records.

## Endpoint

- **Method:** `GET`
- **Path:** `/pub/assessments`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [List assessments](https://www.zillowgroup.com/developers/api/public-data/public-records-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zpid` | query | `string` | no | Zillow property ID to narrow the public records assessment search. |
| `address.full` | query | `string` | no | Full property address to narrow the public records assessment search. |
| `sortBy` | query | `string` | no | Assessment field to sort the returned records by, such as year. |
