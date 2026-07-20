# Zoho Billing: Retrieve Customer



```
GET https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-customer?${params}`, {
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
| `customerId` | string | yes | Unique identifier of the customer. |

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

Through the native Zoho Billing API, this operation is `GET /customers/:customer_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-customer.md) for the provider-specific parameters and requirements.

