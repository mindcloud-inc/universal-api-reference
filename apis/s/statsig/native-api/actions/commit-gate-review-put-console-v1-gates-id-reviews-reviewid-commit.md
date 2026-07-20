# Commit Gate Review with Statsig

Commits a gate review in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/gates/{id}/reviews/{reviewID}/commit`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Commit Gate Review](https://docs.statsig.com/api-reference/gates/commit-gate-review)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `reviewID` | path | `string` | yes |
