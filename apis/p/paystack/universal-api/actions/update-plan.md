# Paystack: Update Plan



```
PUT https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "planIdOrCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paystack/latest/actions/update-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "planIdOrCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `planIdOrCode` | string | yes |  |
| `name` | string | no |  |
| `amount` | number | no |  |
| `interval` | string | no |  |
| `description` | string | no |  |
| `currency` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdAt": "string",
      "currency": "string",
      "hosted_page": true,
      "id": 1,
      "interval": "string",
      "invoice_limit": 1,
      "is_archived": true,
      "name": "Ava Chen",
      "plan_code": "string",
      "send_invoices": true,
      "send_sms": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `hosted_page` | boolean |  |
| `id` | number |  |
| `interval` | string |  |
| `invoice_limit` | number |  |
| `is_archived` | boolean |  |
| `name` | string |  |
| `plan_code` | string |  |
| `send_invoices` | boolean |  |
| `send_sms` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `PUT /plan/:planIdOrCode` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-plan.md) for the provider-specific parameters and requirements.

