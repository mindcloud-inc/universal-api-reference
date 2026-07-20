# Zoho Billing: Update Plan



```
PUT https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/update-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/update-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "planCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/update-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "planCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `planCode` | string | yes | Unique code of the plan. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "plan": {
        "billing_cycles": 1,
        "billing_mode": "string",
        "created_time": "2026-05-07T12:00:00.000Z",
        "interval": 1,
        "interval_unit": "string",
        "is_free_plan": true,
        "name": "Ava Chen",
        "plan_code": "string",
        "plan_id": "string",
        "price_brackets": [
          [
            {}
          ]
        ],
        "product_id": "string",
        "product_name": "Ava Chen",
        "recurring_price": 1,
        "status": "string",
        "updated_time": "2026-05-07T12:00:00.000Z"
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
| `plan` | object |  |
| `plan.billing_cycles` | number |  |
| `plan.billing_mode` | string |  |
| `plan.created_time` | date |  |
| `plan.interval` | number |  |
| `plan.interval_unit` | string |  |
| `plan.is_free_plan` | boolean |  |
| `plan.name` | string |  |
| `plan.plan_code` | string |  |
| `plan.plan_id` | string |  |
| `plan.price_brackets[]` | array<object> |  |
| `plan.price_brackets[].price` | number |  |
| `plan.product_id` | string |  |
| `plan.product_name` | string |  |
| `plan.recurring_price` | number |  |
| `plan.status` | string |  |
| `plan.updated_time` | date |  |

## Native endpoint

Through the native Zoho Billing API, this operation is `PUT /plans/:plan_code` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-plan.md) for the provider-specific parameters and requirements.

