# Chatvolt AI: List Scenario Conversations

Retrieves CRM scenario conversations from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-list-scenario-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-list-scenario-conversations?connectionId=$CONNECTION_ID&scenarioId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scenarioId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-scenario-list-scenario-conversations?${params}`, {
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
| `scenarioId` | string | yes | The ID of the CRM scenario. |
| `stepId` | string | no | The ID of a specific step to filter conversations. |
| `page` | number | no | The page number for pagination. |
| `limit` | number | no | The number of items per page for pagination. |
| `isCount` | boolean | no | If true, returns conversation counts instead of the conversation list. |
| `showInactiveConversations` | boolean | no | If true, includes conversations that are not marked as available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<string> | Response items. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /crm/scenario/{scenarioId}/conversation` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-scenario-list-scenario-conversations.md) for the provider-specific parameters and requirements.

