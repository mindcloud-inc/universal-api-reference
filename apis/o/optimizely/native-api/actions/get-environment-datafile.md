# Get Environment Datafile with Optimizely

Retrieves an environment datafile from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/environments/{environmentId}/datafile`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [Get Environment Datafile](https://docs.developers.optimizely.com/web-experimentation/reference/get_datafile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | The environment id to fetch the datafile for. |
