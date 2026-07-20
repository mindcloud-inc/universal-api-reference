# Paystack: Fetch Transaction



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-transaction?connectionId=$CONNECTION_ID&transactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-transaction?${params}`, {
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
| `transactionId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "authorization": {},
      "channel": "string",
      "created_at": "string",
      "currency": "string",
      "customer": {},
      "gateway_response": "string",
      "id": 1,
      "paid_at": "string",
      "reference": "string",
      "requested_amount": 1,
      "status": "string",
      "transaction_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `authorization` | object |  |
| `channel` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `customer` | object |  |
| `gateway_response` | string |  |
| `id` | number |  |
| `paid_at` | string |  |
| `reference` | string |  |
| `requested_amount` | number |  |
| `status` | string |  |
| `transaction_date` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /transaction/:transactionId` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-transaction.md) for the provider-specific parameters and requirements.

