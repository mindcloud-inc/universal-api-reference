# OPN: Update Transfer

Updates an existing transfer in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-transfer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created_at": "string",
      "currency": "string",
      "deleted": true,
      "failure_code": "string",
      "failure_message": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "object": "string",
      "paid": true,
      "paid_at": "string",
      "recipient": {},
      "sendable": true,
      "sent": true,
      "sent_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created_at` | string |  |
| `currency` | string |  |
| `deleted` | boolean |  |
| `failure_code` | string |  |
| `failure_message` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `merchant_uid` | string |  |
| `object` | string |  |
| `paid` | boolean |  |
| `paid_at` | string |  |
| `recipient` | object |  |
| `sendable` | boolean |  |
| `sent` | boolean |  |
| `sent_at` | string |  |

## Native endpoint

Through the native OPN API, this operation is `PATCH /transfers/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-transfer.md) for the provider-specific parameters and requirements.

