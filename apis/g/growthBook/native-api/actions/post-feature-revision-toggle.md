# Toggle an environment on/off in a draft revision with GrowthBook

Toggles an environment in a GrowthBook feature revision.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/toggle`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Toggle an environment on/off in a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `environment` | body | `string` | yes |
| `enabled` | body | `boolean` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
