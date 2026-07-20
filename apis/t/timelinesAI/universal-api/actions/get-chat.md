# TimelinesAI: Get Chat

Retrieves details for a TimelinesAI chat.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-chat?connectionId=$CONNECTION_ID&chatId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-chat?${params}`, {
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
        "chatgptAutoresponseEnabled": true,
        "closed": true,
        "id": 1,
        "isGroup": true,
        "jid": "string",
        "labels": [
          "string"
        ],
        "name": "Ava Chen",
        "phone": "string",
        "read": true,
        "responsibleEmail": "ava@example.com"
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
| `data.chatgptAutoresponseEnabled` | boolean |  |
| `data.closed` | boolean |  |
| `data.id` | number |  |
| `data.isGroup` | boolean |  |
| `data.jid` | string |  |
| `data.labels` | array<string> |  |
| `data.name` | string |  |
| `data.phone` | string |  |
| `data.read` | boolean |  |
| `data.responsibleEmail` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /chats/{chat_id}` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat.md) for the provider-specific parameters and requirements.

