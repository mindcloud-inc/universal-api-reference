# Update Trigger with Virtually

Updates an existing trigger in Virtually.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/orgs/:orgId/triggers/:triggerId`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Update Trigger](https://app.tryvirtually.com/api/docs#/Triggers/TriggersController_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `triggerId` | path | `string` | yes |
| `clauses[]` | body | `array<object>` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `logicalOp` | body | `string` | no |
| `clauses[].props` | body | `object` | no |
| `clauses[].props.includeNonRequired` | body | `boolean` | no |
| `clauses[].event` | body | `string` | yes |
| `clauses[].props.path` | body | `string` | no |
| `clauses[].props.aggregation` | body | `string` | no |
| `clauses[].quantity` | body | `number` | no |
| `clauses[].comparisonOp` | body | `string` | yes |
| `clauses[].trailingDays` | body | `number` | no |
