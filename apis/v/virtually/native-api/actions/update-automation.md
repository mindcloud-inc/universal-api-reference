# Update Automation with Virtually

Updates an existing automation in Virtually.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/orgs/:orgId/automations/:id`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Update Automation](https://app.tryvirtually.com/api/docs#/Automations/AutomationsController_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `triggerId` | body | `string` | yes |
| `actions[]` | body | `array<object>` | yes |
| `actions[].actionId` | body | `string` | yes |
