# LeadDyno: Create Purchase

Creates a new purchase in LeadDyno.

```
POST https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-purchase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-purchase', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | no | The affiliate code to which the purchase should be assigned. |
| `currency` | string | no | The purchase currency. |
| `email` | string | yes | The email address of the customer who made the purchase. |
| `purchase_code` | string | no | A unique identifier for this purchase. |
| `purchase_amount` | number | no | The total amount of the purchase. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate": {},
      "cancelled": true,
      "created_at": "string",
      "currency": "string",
      "id": 1,
      "lead": {},
      "plan": {},
      "purchase_amount": "string",
      "purchase_code": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `cancelled` | boolean |  |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | number |  |
| `lead` | object |  |
| `plan` | object |  |
| `purchase_amount` | string |  |
| `purchase_code` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `POST /purchases` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase.md) for the provider-specific parameters and requirements.

