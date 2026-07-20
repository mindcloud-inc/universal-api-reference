# Update a rule in a draft revision with GrowthBook

Updates a rule in a GrowthBook feature revision.

## Endpoint

- **Method:** `PUT`
- **Path:** `/features/:id/revisions/:version/rules/:ruleId`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a rule in a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `ruleId` | path | `string` | yes |
| `environment` | body | `string` | yes |
| `rule` | body | `object` | yes |
| `rampSchedule` | body | `object` | no |
| `schedule` | body | `object` | no |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
