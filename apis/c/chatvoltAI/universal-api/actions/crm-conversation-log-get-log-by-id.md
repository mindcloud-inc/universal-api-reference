# Chatvolt AI: Get CRM Conversation Log by ID

Retrieves a CRM conversation log from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-get-log-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-get-log-by-id?connectionId=$CONNECTION_ID&logId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "logId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-get-log-by-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logId` | string | yes | The ID of the CRM conversation log to retrieve. |

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

Through the native Chatvolt AI API, this operation is `GET /crm/conversationLog/{logId}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-conversation-log-get-log-by-id.md) for the provider-specific parameters and requirements.

