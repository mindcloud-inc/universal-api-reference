# Set the default value in a draft revision with GrowthBook

Sets the default value for a GrowthBook feature revision.

## Endpoint

- **Method:** `PUT`
- **Path:** `/features/:id/revisions/:version/default-value`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Set the default value in a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `defaultValue` | body | `string` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
