# Chatvolt AI: List CRM Conversation Logs

Retrieves CRM conversation logs from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-list-crm-conversation-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-list-crm-conversation-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/crm-conversation-log-list-crm-conversation-logs?${params}`, {
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
| `conversationId` | string | no | Filter logs by a specific Conversation ID. |
| `scenarioId` | string | no | Filter logs by a specific CRM Scenario ID. |
| `stepId` | string | no | Filter logs by a specific CRM Step ID. |
| `status` | string | no | Filter logs by status. |
| `page` | number | no | Page number for pagination. |
| `limit` | number | no | Number of logs per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array | Data. |
| `pagination` | object | Pagination. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /crm/conversationLog` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crm-conversation-log-list-crm-conversation-logs.md) for the provider-specific parameters and requirements.

