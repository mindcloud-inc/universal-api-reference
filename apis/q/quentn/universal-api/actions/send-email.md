# Quentn: Send Email



```
POST https://connect.mindcloud.co/v1/universal/quentn/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email_id": "123",
  "recipientContactId": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quentn/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email_id": "123",
    "recipientContactId": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email_id` | number | yes | The numeric Quentn email id to send. Example: `123`. |
| `recipientContactId` | number | yes | Single recipient contact id for the email send request. Example: `2`. |
| `senderId` | number | no | Optional sender id to use when sending the email. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Quentn API, this operation is `POST /mail/:email_id/send` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

