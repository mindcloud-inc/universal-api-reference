# Paystack: List Payment Requests



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-payment-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-payment-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-payment-requests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdAt": "string",
      "currency": "string",
      "customer": {},
      "description": "string",
      "due_date": "string",
      "id": 1,
      "invoice_number": 1,
      "offline_reference": "string",
      "paid": true,
      "request_code": "string",
      "status": "string",
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
| `customer` | object |  |
| `description` | string |  |
| `due_date` | string |  |
| `id` | number |  |
| `invoice_number` | number |  |
| `offline_reference` | string |  |
| `paid` | boolean |  |
| `request_code` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /paymentrequest` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payment-requests.md) for the provider-specific parameters and requirements.

