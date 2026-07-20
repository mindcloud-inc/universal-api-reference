# OPN: Reverse Charge

Reverses an existing charge in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/reverse-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/reverse-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/reverse-charge', {
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
      "authorized": true,
      "created_at": "string",
      "currency": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "object": "string",
      "paid": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `authorized` | boolean |  |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |
| `paid` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native OPN API, this operation is `POST /charges/:id/reverse` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-charge.md) for the provider-specific parameters and requirements.

