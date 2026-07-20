# Create or Update Dispatch with Chatvolt AI

Creates a dispatch in Chatvolt AI, or updates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/dispatches`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create or Update Dispatch](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Include the ID to update an existing dispatch. Omit to create a new one. |
| `name` | body | `string` | no | The name of the dispatch. |
| `status` | body | `string` | no | The status of the dispatch (e.g., 'draft', 'scheduled', 'sent'). |
| `agentId` | body | `string` | no | The ID of the agent responsible for the dispatch. |
| `crmScenarioId` | body | `string` | no | The ID of the CRM scenario associated with the dispatch. |
| `crmStepId` | body | `string` | no | The ID of the CRM step associated with the dispatch. |
| `scheduledAt` | body | `string` | no | The date and time the dispatch is scheduled to run. |
| `templateMessage` | body | `string` | no | The message template for the dispatch. |
| `interval` | body | `number` | no | The interval in minutes between sending messages for the dispatch. |
| `defaultAssigneeId` | body | `string` | no | The ID of the default assignee for conversations created by this dispatch. |
| `defaultStatus` | body | `string` | no | The default status for conversations created by this dispatch. |
| `contactListIds[]` | body | `array<string>` | no | An array of contact list IDs to associate with the dispatch. |
| `exclusionContactListIds[]` | body | `array<string>` | no | An array of contact list IDs to exclude from the dispatch. |
