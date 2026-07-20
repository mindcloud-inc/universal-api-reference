# Chatvolt AI: Update CRM Step

Updates an existing CRM step in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-update-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-update-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-step-update-step', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the CRM step to update. |
| `name` | string | yes | New name for the step. |
| `trigger` | string | no | New trigger condition or keyword for the step. |
| `prompt` | string | no | New main prompt or instruction for the step. |
| `initialMessage` | string | no | New initial message for the step. |
| `autoNextStepId` | string | no | New ID of the step to automatically transition to. Use null to remove. |
| `autoNextTime` | number | no | New time in seconds for auto-transition. Use null to remove. |
| `defaultStatus` | string | no | New default status for conversations at this step. |
| `defaultPriority` | string | no | New default priority for conversations at this step. |
| `assigneeLogicType` | string | no | New logic for assigning conversations at this step. |
| `selectedMembershipIdsForAssignee[]` | array<string> | no | New list of membership IDs for assignee logic. |
| `isRequired` | boolean | no | New mandatory status for the step. |
| `agentId` | string | no | New Agent ID to associate with this step. Use null to remove. |
| `autoNextTimeUnit` | string | no | New time unit for auto-transition. |
| `defaultTags[]` | array<string> | no | New default tags to add to the conversation. |
| `defaultTagsToRemove[]` | array<string> | no | New default tags to remove from the conversation. |
| `requestContact` | object | no | New configuration for requesting contact information. |
| `isConversationRemovalStep` | boolean | no | New value for conversation removal step flag. |
| `zapi` | object | no | Z-API integration settings. |
| `whatsapp` | object | no | WhatsApp template integration settings. |
| `defaultAiControl` | boolean | no | New default AI control setting for the conversation. |
| `webhookUrl` | string | no | New URL for the webhook to be called. |
| `webhookHeader` | object | no | New headers for the webhook request. |

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

Through the native Chatvolt AI API, this operation is `PUT /crm/step` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-step-update-step.md) for the provider-specific parameters and requirements.

