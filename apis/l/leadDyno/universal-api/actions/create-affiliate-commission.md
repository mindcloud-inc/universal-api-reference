# LeadDyno: Create Affiliate Commission

Creates a new commission for an affiliate in LeadDyno.

```
POST https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-affiliate-commission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-affiliate-commission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-affiliate-commission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | no | The commission currency code. |
| `id` | number | yes | The affiliate ID. |
| `note` | string | no | A note or description for the manual commission. |
| `amount` | number | yes | The commission amount to be added. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate": {},
      "amount": "string",
      "cancelled": true,
      "created_at": "string",
      "currency": "string",
      "date": "string",
      "due_at": "string",
      "id": 1,
      "note": "string",
      "paid": true,
      "purchase": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `amount` | string |  |
| `cancelled` | boolean |  |
| `created_at` | string |  |
| `currency` | string |  |
| `date` | string |  |
| `due_at` | string |  |
| `id` | number |  |
| `note` | string |  |
| `paid` | boolean |  |
| `purchase` | object |  |

## Native endpoint

Through the native LeadDyno API, this operation is `POST /affiliates/:id/commissions` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-affiliate-commission.md) for the provider-specific parameters and requirements.

