# Quo: Send Message

Sends a text message in Quo.

```
POST https://connect.mindcloud.co/v1/universal/quo/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quo/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "to[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quo/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "to[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes |  |
| `from` | string | no |  |
| `phoneNumberId` | string | no |  |
| `setInboxStatus` | string | no |  |
| `to[]` | array<string> | yes |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "from": "string",
      "id": "string",
      "phoneNumberId": "string",
      "status": "string",
      "text": "string",
      "to": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `direction` | string |  |
| `from` | string |  |
| `id` | string |  |
| `phoneNumberId` | string |  |
| `status` | string |  |
| `text` | string |  |
| `to` | array<string> |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Quo API, this operation is `POST /messages` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

