# TimelinesAI: List Chat Labels

Retrieves labels for a specific TimelinesAI chat.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chat-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chat-labels?connectionId=$CONNECTION_ID&chatId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chat-labels?${params}`, {
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
| `chatId` | number | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "labels": [
          "string"
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.labels` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /chats/{chat_id}/labels` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-labels.md) for the provider-specific parameters and requirements.

