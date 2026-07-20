# Zoho Billing: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/create-invoice', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `send` | boolean | no | Send the invoice to the associated contact people after creation. |
| `ignoreAutoNumberGeneration` | boolean | no | When true, Zoho expects you to provide the invoice number explicitly. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "invoice": {
        "allow_partial_payments": true,
        "balance": 1,
        "billing_address": {},
        "can_send_invoice_sms": true,
        "created_time": "2026-05-07T12:00:00.000Z",
        "currency_code": "string",
        "customer_id": "string",
        "customer_name": "Ava Chen",
        "due_date": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "invoice_date": "2026-05-07T12:00:00.000Z",
        "invoice_id": "string",
        "invoice_items": [
          [
            {}
          ]
        ],
        "invoice_number": "string",
        "invoice_url": "https://example.com",
        "number": "string",
        "payment_made": 1,
        "shipping_address": {},
        "status": "string",
        "subscriptions": [
          [
            {}
          ]
        ],
        "total": 1,
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
| `invoice` | object |  |
| `invoice.allow_partial_payments` | boolean |  |
| `invoice.balance` | number |  |
| `invoice.billing_address` | object |  |
| `invoice.can_send_invoice_sms` | boolean |  |
| `invoice.created_time` | date |  |
| `invoice.currency_code` | string |  |
| `invoice.customer_id` | string |  |
| `invoice.customer_name` | string |  |
| `invoice.due_date` | date |  |
| `invoice.email` | string |  |
| `invoice.invoice_date` | date |  |
| `invoice.invoice_id` | string |  |
| `invoice.invoice_items[]` | array<object> |  |
| `invoice.invoice_items[].code` | string |  |
| `invoice.invoice_items[].item_id` | string |  |
| `invoice.invoice_items[].item_total` | number |  |
| `invoice.invoice_items[].name` | string |  |
| `invoice.invoice_items[].price` | number |  |
| `invoice.invoice_items[].product_id` | string |  |
| `invoice.invoice_items[].quantity` | number |  |
| `invoice.invoice_number` | string |  |
| `invoice.invoice_url` | string |  |
| `invoice.number` | string |  |
| `invoice.payment_made` | number |  |
| `invoice.shipping_address` | object |  |
| `invoice.status` | string |  |
| `invoice.subscriptions[]` | array<object> |  |
| `invoice.subscriptions[].subscription_id` | string |  |
| `invoice.subscriptions[].subscription_status` | string |  |
| `invoice.total` | number |  |
| `invoice.updated_time` | date |  |
| `message` | string |  |

## Native endpoint

Through the native Zoho Billing API, this operation is `POST /invoices` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

