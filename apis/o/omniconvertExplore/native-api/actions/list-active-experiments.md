# List Active Experiments with Omniconvert Explore

Retrieves active experiments from Omniconvert Explore.

## Endpoint

- **Method:** `GET`
- **Path:** `/active-experiments`
- **Base URL:** `https://api.omniconvert.com/v1`
- **Official documentation:** [List Active Experiments](https://api.omniconvert.com/docs#get--v1-active-experiments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[website-id]` | query | `number` | yes | Website ID used to scope active experiments. |
