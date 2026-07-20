# Landbot: Create Message Hook

Creates a message hook for a Landbot channel.

```
POST https://connect.mindcloud.co/v1/universal/landbot/latest/actions/create-message-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/create-message-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/landbot/latest/actions/create-message-hook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": 1,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | number | yes | Channel ID where the hook will be created. |
| `url` | string | yes | Webhook URL for incoming message notifications. |
| `token` | string | no | Optional token Landbot will send with the hook. |
| `name` | string | no | Optional display name for the hook. |

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

Through the native Landbot API, this operation is `POST /v1/channels/:channel_id/message_hooks/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message-hook.md) for the provider-specific parameters and requirements.

