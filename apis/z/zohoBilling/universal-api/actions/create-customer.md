# Zoho Billing: Create Customer



```
POST https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/create-customer', {
  method: 'POST',
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
      "code": 1,
      "customer": {
        "billing_address": {
          "city": "string",
          "country": "string"
        },
        "billing_day": 1,
        "contact_id": "string",
        "contact_name": "Ava Chen",
        "created_time": "2026-05-07T12:00:00.000Z",
        "currency_code": "string",
        "currency_symbol": "string",
        "custom_fields": [
          [
            {}
          ]
        ],
        "customer_id": "string",
        "customer_sub_type": "string",
        "display_name": "Ava Chen",
        "email": "ava@example.com",
        "outstanding": 1,
        "payment_reminder_enabled": true,
        "primary_contactperson_id": "string",
        "shipping_address": {
          "city": "string",
          "country": "string"
        },
        "status": "string",
        "tags": [
          [
            {}
          ]
        ],
        "updated_time": "2026-05-07T12:00:00.000Z"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `customer` | object |  |
| `customer.billing_address` | object |  |
| `customer.billing_address.city` | string |  |
| `customer.billing_address.country` | string |  |
| `customer.billing_day` | number |  |
| `customer.contact_id` | string |  |
| `customer.contact_name` | string |  |
| `customer.created_time` | date |  |
| `customer.currency_code` | string |  |
| `customer.currency_symbol` | string |  |
| `customer.custom_fields[]` | array<object> |  |
| `customer.customer_id` | string |  |
| `customer.customer_sub_type` | string |  |
| `customer.display_name` | string |  |
| `customer.email` | string |  |
| `customer.outstanding` | number |  |
| `customer.payment_reminder_enabled` | boolean |  |
| `customer.primary_contactperson_id` | string |  |
| `customer.shipping_address` | object |  |
| `customer.shipping_address.city` | string |  |
| `customer.shipping_address.country` | string |  |
| `customer.status` | string |  |
| `customer.tags[]` | array<object> |  |
| `customer.updated_time` | date |  |
| `message` | string |  |

## Native endpoint

Through the native Zoho Billing API, this operation is `POST /customers` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

