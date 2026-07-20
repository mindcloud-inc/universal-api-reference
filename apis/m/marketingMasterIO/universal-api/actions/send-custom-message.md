# Marketing Master IO: Send Custom Message

Sends a custom message to a subscriber in Marketing Master IO.

```
POST https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/send-custom-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/send-custom-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": {},
  "subscriber_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/send-custom-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": {},
    "subscriber_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | object | yes | Custom message payload to send. |
| `message_tag` | string | no | Optional Facebook message tag for sends outside the standard window. |
| `subscriber_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message_id": "string",
      "recipient_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message_id` | string |  |
| `recipient_id` | string |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `POST /v1/messenger/sending/:subscriber_id/custom` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-custom-message.md) for the provider-specific parameters and requirements.

