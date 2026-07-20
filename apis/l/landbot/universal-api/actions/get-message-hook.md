# Landbot: Get Message Hook

Retrieves a message hook from a Landbot channel.

```
GET https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-message-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-message-hook?connectionId=$CONNECTION_ID&channelId=1&hookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1",
  "hookId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-message-hook?${params}`, {
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
| `channelId` | number | yes | Channel ID that owns the hook. |
| `hookId` | number | yes | Hook ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": 1,
      "createdAt": 1,
      "id": 1,
      "name": "Ava Chen",
      "token": "string",
      "updatedAt": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | number |  |
| `createdAt` | number |  |
| `id` | number |  |
| `name` | string |  |
| `token` | string |  |
| `updatedAt` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Landbot API, this operation is `GET /v1/channels/:channel_id/message_hooks/:hook_id/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-hook.md) for the provider-specific parameters and requirements.

