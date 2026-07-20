# Create Automation with Virtually

Creates a new automation in Virtually.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orgs/:orgId/automations`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Create Automation](https://app.tryvirtually.com/api/docs#/Automations/AutomationsController_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `triggerId` | body | `string` | yes |
| `actions[]` | body | `array<object>` | yes |
| `actions[].actionId` | body | `string` | yes |
