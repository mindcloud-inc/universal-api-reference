# Kommunicate: Send Message

Creates a message in Kommunicate.

```
POST https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "message": "string",
  "fromUserName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "message": "string",
    "fromUserName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Conversation identifier to send the message into. |
| `clientGroupId` | string | no | Optional client conversation identifier. |
| `message` | string | yes | Message text to send. |
| `fromUserName` | string | yes | Sender user ID. |
| `metadata` | object | no | Optional rich-message metadata. |

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

Through the native Kommunicate API, this operation is `POST /rest/ws/message/v2/send` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

