# Get Experiment Stats with Omniconvert Explore

Retrieves experiment statistics from Omniconvert Explore.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments/:experimentId/stats`
- **Base URL:** `https://api.omniconvert.com/v1`
- **Official documentation:** [Get Experiment Stats](https://api.omniconvert.com/docs#get--v1-experiments-{experimentId}-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experimentId` | path | `number` | yes | Identifier of the experiment taken from the experiments list. |
| `filter` | query | `string` | no | Experiment stats filter carrier documented by Omniconvert (interval-start, interval-end). |
