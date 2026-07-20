# Remindlo: Send Message



```
POST https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remindlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes |  |
| `channel` | string | no | Default: `sms`. |
| `contactId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "contact_id": "string",
      "message_id": "string",
      "parts": 1,
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string | Delivery channel. |
| `contact_id` | string | Contact identifier the message targets. |
| `message_id` | string | Queued message identifier. |
| `parts` | number | Number of SMS parts required for the body. |
| `status` | string | Message queue status. |
| `success` | boolean | Whether the message request was accepted for delivery. |

## Native endpoint

Through the native Remindlo API, this operation is `POST /messages` (base URL `https://api.remindlo.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

