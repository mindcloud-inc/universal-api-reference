# Chatvolt AI: Update CRM Conversation Log

Updates an existing CRM conversation log in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-update-crm-conversation-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-update-crm-conversation-log" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "logId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-update-crm-conversation-log', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "logId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logId` | string | yes | The ID of the CRM conversation log to update. |
| `status` | string | no | The new status for the CRM conversation log. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversation": {},
      "conversationId": "string",
      "createdAt": "string",
      "id": "string",
      "organizationId": "string",
      "scenario": {},
      "scenarioId": "string",
      "status": "string",
      "step": {},
      "stepId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversation` | object | Conversation. |
| `conversationId` | string | ConversationId. |
| `createdAt` | string | CreatedAt. |
| `id` | string | The unique identifier for the CRM conversation log. |
| `organizationId` | string | OrganizationId. |
| `scenario` | object | Scenario. |
| `scenarioId` | string | ScenarioId. |
| `status` | string | Status. |
| `step` | object | Step. |
| `stepId` | string | StepId. |
| `updatedAt` | string | UpdatedAt. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `PUT /crm/conversationLog/{logId}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-conversation-log-update-crm-conversation-log.md) for the provider-specific parameters and requirements.

