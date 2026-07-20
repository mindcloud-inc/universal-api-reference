# Update CRM Step with Chatvolt AI

Updates an existing CRM step in Chatvolt AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/step`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update CRM Step](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/update-step)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the CRM step to update. |
| `name` | body | `string` | yes | New name for the step. |
| `trigger` | body | `string` | no | New trigger condition or keyword for the step. |
| `prompt` | body | `string` | no | New main prompt or instruction for the step. |
| `initialMessage` | body | `string` | no | New initial message for the step. |
| `autoNextStepId` | body | `string` | no | New ID of the step to automatically transition to. Use null to remove. |
| `autoNextTime` | body | `number` | no | New time in seconds for auto-transition. Use null to remove. |
| `defaultStatus` | body | `string` | no | New default status for conversations at this step. |
| `defaultPriority` | body | `string` | no | New default priority for conversations at this step. |
| `assigneeLogicType` | body | `string` | no | New logic for assigning conversations at this step. |
| `selectedMembershipIdsForAssignee[]` | body | `array<string>` | no | New list of membership IDs for assignee logic. |
| `isRequired` | body | `boolean` | no | New mandatory status for the step. |
| `agentId` | body | `string` | no | New Agent ID to associate with this step. Use null to remove. |
| `autoNextTimeUnit` | body | `string` | no | New time unit for auto-transition. |
| `defaultTags[]` | body | `array<string>` | no | New default tags to add to the conversation. |
| `defaultTagsToRemove[]` | body | `array<string>` | no | New default tags to remove from the conversation. |
| `requestContact` | body | `object` | no | New configuration for requesting contact information. |
| `isConversationRemovalStep` | body | `boolean` | no | New value for conversation removal step flag. |
| `zapi` | body | `object` | no | Z-API integration settings. |
| `whatsapp` | body | `object` | no | WhatsApp template integration settings. |
| `defaultAiControl` | body | `boolean` | no | New default AI control setting for the conversation. |
| `webhookUrl` | body | `string` | no | New URL for the webhook to be called. |
| `webhookHeader` | body | `object` | no | New headers for the webhook request. |
