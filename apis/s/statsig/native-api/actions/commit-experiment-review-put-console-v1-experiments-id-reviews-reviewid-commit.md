# Commit Experiment Review with Statsig

Commits an experiment review in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/experiments/{id}/reviews/{reviewID}/commit`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Commit Experiment Review](https://docs.statsig.com/api-reference/experiments/commit-experiment-review)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `reviewID` | path | `string` | yes |
