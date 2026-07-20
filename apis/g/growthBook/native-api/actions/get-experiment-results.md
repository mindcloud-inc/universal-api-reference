# Get results for an experiment with GrowthBook

Retrieves results for a GrowthBook experiment.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments/:id/results`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get results for an experiment](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `phase` | query | `string` | no | — |
| `dimension` | query | `string` | no | — |
