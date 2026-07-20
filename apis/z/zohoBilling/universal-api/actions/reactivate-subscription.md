# Zoho Billing: Reactivate Subscription



```
PUT https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/reactivate-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/reactivate-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/reactivate-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | string | yes | Unique identifier of the subscription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "subscription": {
        "activated_at": "2026-05-07T12:00:00.000Z",
        "addons": [
          [
            {}
          ]
        ],
        "amount": 1,
        "auto_collect": true,
        "billing_mode": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "current_term_ends_at": "2026-05-07T12:00:00.000Z",
        "current_term_starts_at": "2026-05-07T12:00:00.000Z",
        "customer": {
          "customer_id": "string",
          "display_name": "Ava Chen",
          "email": "ava@example.com"
        },
        "customer_id": "string",
        "line_items": [
          [
            {}
          ]
        ],
        "name": "Ava Chen",
        "next_billing_at": "2026-05-07T12:00:00.000Z",
        "plan": {
          "name": "Ava Chen",
          "plan_code": "string",
          "plan_id": "string",
          "price": 1
        },
        "product_id": "string",
        "product_name": "Ava Chen",
        "status": "string",
        "subscription_id": "string",
        "subscription_number": "string",
        "taxes": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `subscription` | object |  |
| `subscription.activated_at` | date |  |
| `subscription.addons[]` | array<object> |  |
| `subscription.amount` | number |  |
| `subscription.auto_collect` | boolean |  |
| `subscription.billing_mode` | string |  |
| `subscription.created_at` | date |  |
| `subscription.current_term_ends_at` | date |  |
| `subscription.current_term_starts_at` | date |  |
| `subscription.customer` | object |  |
| `subscription.customer_id` | string |  |
| `subscription.customer.customer_id` | string |  |
| `subscription.customer.display_name` | string |  |
| `subscription.customer.email` | string |  |
| `subscription.line_items[]` | array<object> |  |
| `subscription.line_items[].item_id` | string |  |
| `subscription.line_items[].item_total` | number |  |
| `subscription.line_items[].line_item_id` | string |  |
| `subscription.line_items[].name` | string |  |
| `subscription.line_items[].rate` | number |  |
| `subscription.name` | string |  |
| `subscription.next_billing_at` | date |  |
| `subscription.plan` | object |  |
| `subscription.plan.name` | string |  |
| `subscription.plan.plan_code` | string |  |
| `subscription.plan.plan_id` | string |  |
| `subscription.plan.price` | number |  |
| `subscription.product_id` | string |  |
| `subscription.product_name` | string |  |
| `subscription.status` | string |  |
| `subscription.subscription_id` | string |  |
| `subscription.subscription_number` | string |  |
| `subscription.taxes[]` | array<object> |  |

## Native endpoint

Through the native Zoho Billing API, this operation is `POST /subscriptions/:subscription_id/reactivate` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reactivate-subscription.md) for the provider-specific parameters and requirements.

