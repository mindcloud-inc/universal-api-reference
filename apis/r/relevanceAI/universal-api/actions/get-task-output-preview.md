# Relevance AI: Get Task Output Preview



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-task-output-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-task-output-preview?connectionId=$CONNECTION_ID&agentId=string&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-task-output-preview?${params}`, {
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
| `agentId` | string | yes |  |
| `conversationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "executor": {
        "agent_id": "string",
        "conversation_id": "string"
      },
      "insert_date_": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "studio_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | The job run ID. |
| `executor.agent_id` | string | The agent ID for the run. |
| `executor.conversation_id` | string | The conversation ID for the run. |
| `insert_date_` | date | When the job run was created. |
| `status` | string | The job run status. |
| `studio_id` | string | The studio runner ID. |

## Native endpoint

Through the native Relevance AI API, this operation is `GET /agents/conversations/studios/list` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-output-preview.md) for the provider-specific parameters and requirements.

