# Create Trigger with Virtually

Creates a new trigger in Virtually.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orgs/:orgId/triggers`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Create Trigger](https://app.tryvirtually.com/api/docs#/Triggers/TriggersController_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tags[]` | body | `array<string>` | no |
| `excludeTags[]` | body | `array<string>` | no |
| `clauses[]` | body | `array<object>` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `logicalOp` | body | `string` | yes |
| `createdBy` | body | `string` | no |
| `clauses[].props` | body | `object` | no |
| `clauses[].props.includeNonRequired` | body | `boolean` | no |
| `clauses[].event` | body | `string` | yes |
| `clauses[].quantity` | body | `number` | yes |
| `clauses[].comparisonOp` | body | `string` | yes |
| `clauses[].trailingDays` | body | `number` | yes |
