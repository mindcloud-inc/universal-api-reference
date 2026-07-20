# Paystack: Fetch Plan



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-plan?connectionId=$CONNECTION_ID&planIdOrCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planIdOrCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-plan?${params}`, {
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
| `planIdOrCode` | string | yes |  |

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

Through the native Paystack API, this operation is `GET /plan/:planIdOrCode` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-plan.md) for the provider-specific parameters and requirements.

