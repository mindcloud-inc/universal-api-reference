# OPN: Mark Transfer As Paid

Marks an existing transfer as paid in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/mark-transfer-as-paid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/mark-transfer-as-paid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/mark-transfer-as-paid', {
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
      "id": "string",
      "livemode": true,
      "location": "string",
      "object": "string",
      "paid": true,
      "paid_at": "string",
      "sent": true
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
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |
| `paid` | boolean |  |
| `paid_at` | string |  |
| `sent` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `POST /transfers/:id/mark_as_paid` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-transfer-as-paid.md) for the provider-specific parameters and requirements.

