# Create a single rampSchedule with GrowthBook

Creates a new ramp schedule in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/ramp-schedules`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single rampSchedule](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `featureId` | body | `string` | no | Feature that anchors this schedule. Required when ruleId/environment are set. |
| `ruleId` | body | `string` | no | Rule to attach as the initial target. Requires featureId and environment. |
| `environment` | body | `string` | no | Environment of the target rule. Requires featureId and ruleId. |
| `steps[]` | body | `array<object>` | no | Ordered ramp steps. When featureId+ruleId+environment are provided, `targetId` and `patch.ruleId` in actions are auto-injected — only supply the patch fields you want to change. |
| `endActions[]` | body | `array<object>` | no | Actions applied when the ramp completes. targetId and patch.ruleId are auto-injected when featureId+ruleId+environment are provided. |
| `startDate` | body | `date` | no | — |
| `endCondition` | body | `object` | no | Optional hard deadline |
| `templateId` | body | `string` | no | Load steps and endActions from a saved template (featureId+ruleId+environment must also be set for auto-injection) |
