# ChargeDesk: List Charges

Retrieves charges from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-charges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-charges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-charges?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native ChargeDesk API, this operation is `GET /charges` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-charges.md) for the provider-specific parameters and requirements.

