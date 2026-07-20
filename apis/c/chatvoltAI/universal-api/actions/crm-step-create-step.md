# Chatvolt AI: Create CRM Step

Creates a new CRM step in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-create-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-create-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "scenarioId": "string",
  "trigger": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-create-step', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "scenarioId": "string",
    "trigger": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name for the new CRM step. |
| `scenarioId` | string | yes | The ID of the CRM scenario this step belongs to. |
| `agentId` | string | no | Optional Agent ID to associate with this step. |
| `trigger` | string | yes | A trigger condition or keyword for this step. |
| `prompt` | string | no | The main prompt or instruction for this step. |
| `initialMessage` | string | no | An initial message to be sent when this step is activated. |
| `autoNextStepId` | string | no | ID of the step to automatically transition to. |
| `autoNextTime` | number | no | Time in seconds to wait before auto-transitioning. |
| `defaultStatus` | string | no | Default status for conversations at this step. |
| `defaultPriority` | string | no | Default priority for conversations at this step. |
| `assigneeLogicType` | string | no | Logic for assigning conversations at this step. |
| `selectedMembershipIdsForAssignee[]` | array<string> | no | List of membership IDs for assignee logic. Required for single_user, random_selected, and fair_distribution_selected. |
| `isRequired` | boolean | no | Indicates if this step is mandatory. |
| `autoNextTimeUnit` | string | no | The time unit for auto-transition. |
| `defaultTags[]` | array<string> | no | Default tags to add to the conversation. |
| `defaultTagsToRemove[]` | array<string> | no | Default tags to remove from the conversation. |
| `requestContact` | object | no | Configuration for requesting contact information. |
| `isConversationRemovalStep` | boolean | no | If true, this step removes the conversation from the scenario. |
| `zapiAgentId` | string | no | Z-API Agent ID for sending messages. |
| `zapiPhoneNumber` | string | no | Z-API phone number for sending messages. |
| `zapiMessage` | string | no | Z-API message to send. |
| `whatsappTemplateAgentId` | string | no | Agent ID for WhatsApp template message. |
| `whatsappTemplateName` | string | no | Name of the WhatsApp template. |
| `whatsappTemplateLanguageCode` | string | no | Language code for the WhatsApp template. |
| `whatsappTemplateText` | string | no | Text content of the WhatsApp template. |
| `defaultAiControl` | boolean | no | Default AI control setting for the conversation. |
| `webhookUrl` | string | no | URL for the webhook to be called. |
| `webhookHeader` | object | no | Headers for the webhook request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "agentId": "string",
      "assigneeLogicType": "string",
      "autoNextStepId": "string",
      "autoNextTime": 1,
      "autoNextTimeUnit": "string",
      "createdAt": "string",
      "defaultAiControl": true,
      "defaultPriority": "string",
      "defaultStatus": "string",
      "defaultTags": [
        "string"
      ],
      "defaultTagsToRemove": [
        "string"
      ],
      "id": "string",
      "index": 1,
      "initialMessage": "string",
      "isConversationRemovalStep": true,
      "isRequired": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "prompt": "string",
      "requestContact": {},
      "scenario": {},
      "scenarioId": "string",
      "selectedMembershipIdsForAssignee": [
        "string"
      ],
      "trigger": "string",
      "updatedAt": "string",
      "webhookHeader": {},
      "webhookUrl": "https://example.com",
      "whatsapp": {},
      "zapi": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object | Agent. |
| `agentId` | string | AgentId. |
| `assigneeLogicType` | string | Logic for assigning conversations at this step. |
| `autoNextStepId` | string | ID of the step to automatically transition to after this one. |
| `autoNextTime` | number | Time in seconds to wait before automatically transitioning to autoNextStepId. |
| `autoNextTimeUnit` | string | The time unit for auto-transition. |
| `createdAt` | string | Timestamp of when the step was created. |
| `defaultAiControl` | boolean | Default AI control setting for the conversation. |
| `defaultPriority` | string | Default priority to set for conversations reaching this step. |
| `defaultStatus` | string | Default status to set for conversations reaching this step. |
| `defaultTags` | array<string> | Default tags to add to the conversation. |
| `defaultTagsToRemove` | array<string> | Default tags to remove from the conversation. |
| `id` | string | The unique identifier for the CRM step. |
| `index` | number | The order/index of the step within its scenario. |
| `initialMessage` | string | An initial message to be sent when this step is activated. |
| `isConversationRemovalStep` | boolean | If true, this step removes the conversation from the scenario. |
| `isRequired` | boolean | Indicates if this step is mandatory. |
| `name` | string | The name of the CRM step. |
| `organizationId` | string | OrganizationId. |
| `prompt` | string | The main prompt or instruction for this step. |
| `requestContact` | object | Configuration for requesting contact information. |
| `scenario` | object | Scenario. |
| `scenarioId` | string | ScenarioId. |
| `selectedMembershipIdsForAssignee` | array<string> | List of membership IDs for assignee logic. |
| `trigger` | string | A trigger condition or keyword for this step. |
| `updatedAt` | string | Timestamp of when the step was last updated. |
| `webhookHeader` | object | Headers for the webhook request. |
| `webhookUrl` | string | URL for the webhook to be called. |
| `whatsapp` | object | WhatsApp template integration settings. |
| `zapi` | object | Z-API integration settings. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /crm/step` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-step-create-step.md) for the provider-specific parameters and requirements.

