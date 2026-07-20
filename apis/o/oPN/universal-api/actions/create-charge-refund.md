# OPN: Create Charge Refund

Creates a new refund for a charge in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-charge-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-charge-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-charge-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | The refund amount in the smallest currency unit. |
| `id` | string | yes | The charge ID to refund. |
| `void` | boolean | no | Whether to void the charge instead of issuing a partial refund. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acquirer_reference_number": "string",
      "amount": 1,
      "approval_code": "string",
      "capture": "string",
      "charge": "string",
      "created_at": "string",
      "currency": "string",
      "funding_amount": 1,
      "funding_currency": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "metadata": {},
      "object": "string",
      "status": "string",
      "terminal": "string",
      "voided": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acquirer_reference_number` | string |  |
| `amount` | number |  |
| `approval_code` | string |  |
| `capture` | string |  |
| `charge` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `funding_amount` | number |  |
| `funding_currency` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `merchant_uid` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `status` | string |  |
| `terminal` | string |  |
| `voided` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `POST /charges/:id/refunds` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-charge-refund.md) for the provider-specific parameters and requirements.

