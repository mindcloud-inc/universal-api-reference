# ChargeDesk: Update Charge

Updates an existing charge in ChargeDesk.

```
PUT https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/update-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/update-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chargeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/update-charge', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chargeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chargeId` | string | yes | Charge ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "amount_formatted": "string",
      "charge_id": "string",
      "company": "string",
      "currency": "string",
      "customer_email": "ava@example.com",
      "customer_id": "string",
      "customer_name": "Ava Chen",
      "description": "string",
      "invoice_url": "https://example.com",
      "is_paid": true,
      "manage_url": "https://example.com",
      "methods_active": [
        "string"
      ],
      "methods_supported": [
        "string"
      ],
      "object": "string",
      "occurred": "string",
      "product_id": "string",
      "status": "string",
      "status_text": "string",
      "subscription_id": "string",
      "support_url": "https://example.com",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `amount_formatted` | string |  |
| `charge_id` | string |  |
| `company` | string |  |
| `currency` | string |  |
| `customer_email` | string |  |
| `customer_id` | string |  |
| `customer_name` | string |  |
| `description` | string |  |
| `invoice_url` | string |  |
| `is_paid` | boolean |  |
| `manage_url` | string |  |
| `methods_active` | array<string> |  |
| `methods_supported` | array<string> |  |
| `object` | string |  |
| `occurred` | string |  |
| `product_id` | string |  |
| `status` | string |  |
| `status_text` | string |  |
| `subscription_id` | string |  |
| `support_url` | string |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `POST /charges/:CHARGE_ID` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-charge.md) for the provider-specific parameters and requirements.

