# Commit Dynamic Config Review with Statsig

Commits a dynamic config review in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/dynamic_configs/{id}/reviews/{reviewID}/commit`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Commit Dynamic Config Review](https://docs.statsig.com/api-reference/dynamic-configs/commit-dynamic-config-review)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `reviewID` | path | `string` | yes |
