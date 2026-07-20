# Remove ramp schedule from a rule with GrowthBook

Removes a ramp schedule from a GrowthBook rule.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/features/:id/revisions/:version/rules/:ruleId/ramp-schedule`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Remove ramp schedule from a rule](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `ruleId` | path | `string` | yes |
| `environment` | body | `string` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
