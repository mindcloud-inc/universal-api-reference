# Zoho Billing: Retrieve Invoice



```
GET https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-invoice?connectionId=$CONNECTION_ID&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-invoice?${params}`, {
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
| `invoiceId` | string | yes | Unique identifier of the invoice. |

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

Through the native Zoho Billing API, this operation is `GET /invoices/:invoice_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-invoice.md) for the provider-specific parameters and requirements.

