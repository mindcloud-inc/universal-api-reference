# ChargeDesk: Retrieve Charge

Retrieves a charge from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-charge?connectionId=$CONNECTION_ID&chargeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chargeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-charge?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chargeId` | string | yes | Charge ID to retrieve. |

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

Through the native ChargeDesk API, this operation is `GET /charges/:CHARGE_ID` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-charge.md) for the provider-specific parameters and requirements.

