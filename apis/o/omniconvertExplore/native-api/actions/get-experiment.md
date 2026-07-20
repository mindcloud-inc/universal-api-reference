# Get Experiment with Omniconvert Explore

Retrieves an experiment from Omniconvert Explore.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments/:experimentId`
- **Base URL:** `https://api.omniconvert.com/v1`
- **Official documentation:** [Get Experiment](https://api.omniconvert.com/docs#get--v1-experiments-{experimentId})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experimentId` | path | `number` | yes | Identifier of the experiment taken from the experiments list. |
| `filter` | query | `string` | no | Experiment detail filter carrier documented by Omniconvert (interval-start, interval-end). |
