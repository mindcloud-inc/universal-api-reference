# Pushbullet: Delete Chat

Deletes an existing chat from Pushbullet.

```
DELETE https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-chat?connectionId=$CONNECTION_ID&chat_iden=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chat_iden": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/delete-chat?${params}`, {
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
| `chat_iden` | string | yes | Chat identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Pushbullet API, this operation is `DELETE /chats/:chat_iden` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-chat.md) for the provider-specific parameters and requirements.

