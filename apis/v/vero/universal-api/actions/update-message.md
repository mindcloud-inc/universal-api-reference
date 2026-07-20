# Vero: Update Message

Updates an existing message in Vero.

```
PUT https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "message_example"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "message_example"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The message identifier. Default: `message_example`. |
| `provider` | string | no | Optional message provider value. |
| `transactional` | boolean | no | Optional transactional flag. |
| `contents` | object | no | Optional message contents object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "id": "string",
      "object": "string",
      "provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string | Owning campaign identifier. |
| `id` | string | Message identifier. |
| `object` | string | Resource type. |
| `provider` | string | Delivery provider. |

## Native endpoint

Through the native Vero API, this operation is `PATCH /api/v4/messages/:id` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.

