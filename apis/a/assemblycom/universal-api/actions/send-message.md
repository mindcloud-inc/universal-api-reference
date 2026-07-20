# Assembly.com: Send Message

Sends a message in an Assembly.com message channel.

```
POST https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "channelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "channelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | The contents of the message. |
| `channelId` | string | yes | The Message Channel where the message will be sent. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderId` | string | no | Send this message on behalf of a channel member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "identityId": "string",
      "isAttachmentIncluded": true,
      "object": "string",
      "senderId": "string",
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `identityId` | string |  |
| `isAttachmentIncluded` | boolean |  |
| `object` | string |  |
| `senderId` | string |  |
| `text` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Assembly.com API, this operation is `POST /messages` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

