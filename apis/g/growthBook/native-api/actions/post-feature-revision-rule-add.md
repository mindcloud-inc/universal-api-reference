# Add a rule to a draft revision with GrowthBook

Adds a rule to a GrowthBook feature revision.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/rules`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Add a rule to a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `environment` | body | `string` | yes |
| `rule` | body | `object` | yes |
| `rampSchedule` | body | `object` | no |
| `schedule` | body | `object` | no |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
