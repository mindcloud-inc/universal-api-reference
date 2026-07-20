# Set holdout in a draft revision with GrowthBook

Sets holdout for a GrowthBook feature revision.

## Endpoint

- **Method:** `PUT`
- **Path:** `/features/:id/revisions/:version/holdout`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Set holdout in a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `holdout` | body | `object` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
