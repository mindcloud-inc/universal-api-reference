# Kommunicate: Send Mixed Buttons Message

Creates a mixed buttons message in Kommunicate.

```
POST https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-mixed-buttons-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-mixed-buttons-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "message": "string",
  "fromUserName": "Ava Chen",
  "payloadJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-mixed-buttons-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "message": "string",
    "fromUserName": "Ava Chen",
    "payloadJson": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Conversation identifier to send the message into. |
| `message` | string | yes | Message text shown above the mixed buttons. |
| `fromUserName` | string | yes | Sender user ID. |
| `payloadJson` | string<object> | yes | Array of mixed button objects from the official template format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "messageKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `messageKey` | string |  |

## Native endpoint

Through the native Kommunicate API, this operation is `POST /rest/ws/message/v2/send` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-mixed-buttons-message.md) for the provider-specific parameters and requirements.

