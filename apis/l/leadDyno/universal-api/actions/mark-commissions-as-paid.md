# LeadDyno: Mark Commissions As Paid

Marks affiliate commissions as paid for a purchase in LeadDyno.

```
PUT https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/mark-commissions-as-paid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/mark-commissions-as-paid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "affiliate_email": "ava@example.com",
  "purchase_code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/mark-commissions-as-paid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "affiliate_email": "ava@example.com",
    "purchase_code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affiliate_email` | string | yes | The affiliate e-mail the payment is directed to. |
| `purchase_code` | string | yes | The purchase that originated the commissions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "cancelled": true,
      "currency": "string",
      "id": 1,
      "paid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `cancelled` | boolean |  |
| `currency` | string |  |
| `id` | number |  |
| `paid` | boolean |  |

## Native endpoint

Through the native LeadDyno API, this operation is `POST /commissions/mark_as_paid` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-commissions-as-paid.md) for the provider-specific parameters and requirements.

