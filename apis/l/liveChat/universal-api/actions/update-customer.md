# LiveChat: Update Customer

Updates an existing customer in LiveChat.

```
PUT https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The customer UUID v4. |
| `name` | string | no | The customer's name. |
| `email` | string | no | The customer's email. |
| `avatar` | string | no | The URL of the customer's avatar. |
| `phoneNumber` | string | no | The customer's phone number in E.164 format. |
| `sessionFields[]` | array<object> | no | Custom session field objects in array order. |
| `omnichannel` | object | no | Omnichannel customer data. |
| `omnichannel.fbMessenger` | object | no | Facebook Messenger customer data. |
| `omnichannel.fbMessenger.id` | string | no | Facebook Messenger user ID. |
| `omnichannel.twilio` | object | no | Twilio customer data. |
| `omnichannel.twilio.phoneNumber` | string | no | Twilio phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Official Text Platform Agent Chat API docs specify this mutation returns no response payload (200 OK). |

## Native endpoint

Through the native LiveChat API, this operation is `POST /update_customer` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

