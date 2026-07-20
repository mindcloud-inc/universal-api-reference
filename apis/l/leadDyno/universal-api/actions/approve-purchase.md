# LeadDyno: Approve Purchase

Approves a pending purchase in LeadDyno.

```
PUT https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/approve-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/approve-purchase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/approve-purchase', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The purchase ID. |

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

Through the native LeadDyno API, this operation is `POST /purchases/:id/approve` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-purchase.md) for the provider-specific parameters and requirements.

