# Create CRM Step with Chatvolt AI

Creates a new CRM step in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/step`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create CRM Step](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/create-step)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name for the new CRM step. |
| `scenarioId` | body | `string` | yes | The ID of the CRM scenario this step belongs to. |
| `agentId` | body | `string` | no | Optional Agent ID to associate with this step. |
| `trigger` | body | `string` | yes | A trigger condition or keyword for this step. |
| `prompt` | body | `string` | no | The main prompt or instruction for this step. |
| `initialMessage` | body | `string` | no | An initial message to be sent when this step is activated. |
| `autoNextStepId` | body | `string` | no | ID of the step to automatically transition to. |
| `autoNextTime` | body | `number` | no | Time in seconds to wait before auto-transitioning. |
| `defaultStatus` | body | `string` | no | Default status for conversations at this step. |
| `defaultPriority` | body | `string` | no | Default priority for conversations at this step. |
| `assigneeLogicType` | body | `string` | no | Logic for assigning conversations at this step. |
| `selectedMembershipIdsForAssignee[]` | body | `array<string>` | no | List of membership IDs for assignee logic. Required for single_user, random_selected, and fair_distribution_selected. |
| `isRequired` | body | `boolean` | no | Indicates if this step is mandatory. |
| `autoNextTimeUnit` | body | `string` | no | The time unit for auto-transition. |
| `defaultTags[]` | body | `array<string>` | no | Default tags to add to the conversation. |
| `defaultTagsToRemove[]` | body | `array<string>` | no | Default tags to remove from the conversation. |
| `requestContact` | body | `object` | no | Configuration for requesting contact information. |
| `isConversationRemovalStep` | body | `boolean` | no | If true, this step removes the conversation from the scenario. |
| `zapiAgentId` | body | `string` | no | Z-API Agent ID for sending messages. |
| `zapiPhoneNumber` | body | `string` | no | Z-API phone number for sending messages. |
| `zapiMessage` | body | `string` | no | Z-API message to send. |
| `whatsappTemplateAgentId` | body | `string` | no | Agent ID for WhatsApp template message. |
| `whatsappTemplateName` | body | `string` | no | Name of the WhatsApp template. |
| `whatsappTemplateLanguageCode` | body | `string` | no | Language code for the WhatsApp template. |
| `whatsappTemplateText` | body | `string` | no | Text content of the WhatsApp template. |
| `defaultAiControl` | body | `boolean` | no | Default AI control setting for the conversation. |
| `webhookUrl` | body | `string` | no | URL for the webhook to be called. |
| `webhookHeader` | body | `object` | no | Headers for the webhook request. |
