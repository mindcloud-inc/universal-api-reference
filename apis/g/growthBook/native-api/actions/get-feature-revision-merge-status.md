# Get merge status for a draft revision with GrowthBook

Retrieves merge status for a GrowthBook draft revision.

## Endpoint

- **Method:** `GET`
- **Path:** `/features/:id/revisions/:version/merge-status`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get merge status for a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
