# 2Chat: Get Channel Status

Retrieves a WhatsApp channel status from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-channel-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-channel-status?connectionId=$CONNECTION_ID&channel_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-channel-status?${params}`, {
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
| `channel_uuid` | string | yes | The UUID of the WhatsApp channel connected to 2Chat. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionStatus": "string",
      "events": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "event": "string",
          "payload": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionStatus` | string |  |
| `events[].createdAt` | date |  |
| `events[].event` | string |  |
| `events[].payload` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/channel/:channel_uuid/status` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-status.md) for the provider-specific parameters and requirements.

