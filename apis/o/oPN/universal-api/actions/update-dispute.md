# OPN: Update Dispute

Updates an existing dispute in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-dispute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-dispute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-dispute', {
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
| `id` | string | yes | The dispute ID to update. |
| `message` | string | no | The dispute response message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin_message": "string",
      "amount": 1,
      "charge": "string",
      "closed_at": "string",
      "created_at": "string",
      "currency": "string",
      "documents": {},
      "funding_amount": 1,
      "funding_currency": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "message": "string",
      "metadata": {},
      "object": "string",
      "reason_code": "string",
      "reason_message": "string",
      "status": "string",
      "transactions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin_message` | string |  |
| `amount` | number |  |
| `charge` | string |  |
| `closed_at` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `documents` | object |  |
| `funding_amount` | number |  |
| `funding_currency` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `merchant_uid` | string |  |
| `message` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `reason_code` | string |  |
| `reason_message` | string |  |
| `status` | string |  |
| `transactions` | array<object> |  |

## Native endpoint

Through the native OPN API, this operation is `PATCH /disputes/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dispute.md) for the provider-specific parameters and requirements.

