# Start or Stop Experiment with Omniconvert Explore

Updates an experiment by starting or stopping it in Omniconvert Explore.

## Endpoint

- **Method:** `POST`
- **Path:** `/experiments/:experimentId/:action`
- **Base URL:** `https://api.omniconvert.com/v1`
- **Official documentation:** [Start or Stop Experiment](https://api.omniconvert.com/docs#post--v1-experiments-{experimentId}-{action})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | yes | Experiment action documented by Omniconvert. Allowed values: start, stop. |
| `experimentId` | path | `number` | yes | Identifier of the experiment taken from the experiments list. |
