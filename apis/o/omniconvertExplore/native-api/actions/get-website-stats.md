# Get Website Stats with Omniconvert Explore

Retrieves website statistics from Omniconvert Explore.

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/stats`
- **Base URL:** `https://api.omniconvert.com/v1`
- **Official documentation:** [Get Website Stats](https://api.omniconvert.com/docs#get--v1-websites-{websiteId}-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval-end` | query | `string` | no | End date filter for the stats interval. |
| `interval-start` | query | `string` | no | Start date filter for the stats interval. |
| `type` | query | `string` | no | Stats type selector documented by Omniconvert. |
| `websiteId` | path | `number` | yes | Website identifier used in the endpoint path. |
