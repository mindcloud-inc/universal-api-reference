# Paystack: Fetch Payment Request



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-payment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-payment-request?connectionId=$CONNECTION_ID&paymentRequestIdOrCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentRequestIdOrCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-payment-request?${params}`, {
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
| `paymentRequestIdOrCode` | string | yes |  |

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

Through the native Paystack API, this operation is `GET /paymentrequest/:paymentRequestIdOrCode` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-payment-request.md) for the provider-specific parameters and requirements.

