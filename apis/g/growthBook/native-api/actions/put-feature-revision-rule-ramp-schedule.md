# Set ramp schedule for a rule with GrowthBook

Sets a ramp schedule for a GrowthBook rule.

## Endpoint

- **Method:** `PUT`
- **Path:** `/features/:id/revisions/:version/rules/:ruleId/ramp-schedule`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Set ramp schedule for a rule](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `ruleId` | path | `string` | yes |
| `name` | body | `string` | no |
| `templateId` | body | `string` | no |
| `steps[]` | body | `array<object>` | no |
| `steps[]` | body | `array<object>` | no |
| `endActions[]` | body | `array<object>` | no |
| `endActions[]` | body | `array<object>` | no |
| `startDate` | body | `string` | no |
| `endCondition` | body | `object` | no |
| `environment` | body | `string` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
