# Pushpad: Get Sender

Retrieves a specific sender from Pushpad.

```
GET https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-sender?connectionId=$CONNECTION_ID&senderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "senderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-sender?${params}`, {
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
| `senderId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": 1,
      "name": "Ava Chen",
      "vapidPrivateKey": "string",
      "vapidPublicKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `name` | string |  |
| `vapidPrivateKey` | string |  |
| `vapidPublicKey` | string |  |

## Native endpoint

Through the native Pushpad API, this operation is `GET /senders/:sender_id` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sender.md) for the provider-specific parameters and requirements.

