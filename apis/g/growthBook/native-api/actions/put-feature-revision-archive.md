# Set archived state in a draft revision with GrowthBook

Sets archived state for a GrowthBook feature revision.

## Endpoint

- **Method:** `PUT`
- **Path:** `/features/:id/revisions/:version/archive`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Set archived state in a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `archived` | body | `boolean` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
