# TimelinesAI: Get Message

Retrieves details for a TimelinesAI message.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-message?connectionId=$CONNECTION_ID&messageUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-message?${params}`, {
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
| `messageUid` | string | yes | UID of the message in the TimelinesAI workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attachmentUrl": "https://example.com",
        "chatId": 1,
        "fromMe": true,
        "recipientName": "Ava Chen",
        "recipientPhone": "string",
        "senderName": "Ava Chen",
        "senderPhone": "string",
        "text": "string",
        "timestamp": "string",
        "uid": "string"
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
| `data.attachmentUrl` | string |  |
| `data.chatId` | number |  |
| `data.fromMe` | boolean |  |
| `data.recipientName` | string |  |
| `data.recipientPhone` | string |  |
| `data.senderName` | string |  |
| `data.senderPhone` | string |  |
| `data.text` | string |  |
| `data.timestamp` | string |  |
| `data.uid` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /messages/{message_uid}` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

