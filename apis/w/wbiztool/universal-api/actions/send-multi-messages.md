# Wbiztool: Send Multi Messages

Creates WhatsApp messages for multiple recipients in Wbiztool.

```
POST https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/send-multi-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/send-multi-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msgType": "string",
  "recipients": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/send-multi-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msgType": "string",
    "recipients": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msgType` | string | yes | Wbiztool message type code as numeric text: 0 text, 1 image, 2 file. |
| `recipients` | string | yes | Comma-separated list of phone numbers or group names to message. |
| `countryCode` | string | no | Country code applied to recipient phone numbers when needed. |
| `message` | string | yes | Message text or caption to send. |
| `imageUrl` | string | no | Public image URL for image campaigns. |
| `fileUrl` | string | no | Public file URL for file campaigns. |
| `fileName` | string | no | Optional display name for file campaigns. |
| `webhookUrl` | string | no | Optional webhook URL to receive delivery events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "messages": [
        {
          "contact": "string",
          "isGroup": true,
          "msgId": 1
        }
      ],
      "msgIds": [
        1
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `messages[].contact` | string |  |
| `messages[].isGroup` | boolean |  |
| `messages[].msgId` | number |  |
| `msgIds[]` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /send_msg/multi/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-multi-messages.md) for the provider-specific parameters and requirements.

