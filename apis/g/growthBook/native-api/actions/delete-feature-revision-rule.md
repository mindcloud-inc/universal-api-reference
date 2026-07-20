# Delete a rule from a draft revision with GrowthBook

Deletes a rule from a GrowthBook feature revision.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/features/:id/revisions/:version/rules/:ruleId`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Delete a rule from a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `ruleId` | path | `string` | yes |
| `environment` | body | `string` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
