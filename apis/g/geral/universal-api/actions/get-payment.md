# Geral: Get Payment

Retrieves an account payment from Geral by ID.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-payment?connectionId=$CONNECTION_ID&paymentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-payment?${params}`, {
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
| `paymentId` | number | yes | The payment ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "frequency": "string",
      "id": 1,
      "name": "Ava Chen",
      "plan_id": 1,
      "processor": "string",
      "status": true,
      "total_amount": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Payment currency. |
| `datetime` | date | Creation timestamp. |
| `email` | string | Billing email. |
| `frequency` | string | Billing frequency. |
| `id` | number | Payment ID. |
| `name` | string | Billing name. |
| `plan_id` | number | Plan ID. |
| `processor` | string | Payment processor. |
| `status` | boolean | Payment status. |
| `total_amount` | string | Total payment amount. |
| `type` | string | Payment type. |

## Native endpoint

Through the native Geral API, this operation is `GET /payments/:payment_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment.md) for the provider-specific parameters and requirements.

