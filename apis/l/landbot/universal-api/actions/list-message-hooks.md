# Landbot: List Message Hooks

Retrieves message hooks for a Landbot channel.

```
GET https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-message-hooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-message-hooks?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-message-hooks?${params}`, {
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
| `channelId` | number | yes | Channel ID whose message hooks to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hooks": [
        [
          "string"
        ]
      ],
      "success": true,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hooks[]` | array<string> |  |
| `success` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native Landbot API, this operation is `GET /v1/channels/:channel_id/message_hooks/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-hooks.md) for the provider-specific parameters and requirements.

