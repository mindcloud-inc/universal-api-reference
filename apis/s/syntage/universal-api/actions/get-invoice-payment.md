# Syntage: Get Invoice Payment

Retrieves an invoice payment from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-invoice-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-invoice-payment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-invoice-payment?${params}`, {
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
| `id` | string | yes | The invoice payment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@id": "string",
      "@type": "string",
      "amount": 1,
      "batchPayment": "string",
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "string",
      "currency": "string",
      "exchangeRate": 1,
      "id": "string",
      "installment": 1,
      "invoice": "string",
      "invoiceUuid": "string",
      "outstandingBalance": 1,
      "previousBalance": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@id` | string |  |
| `@type` | string |  |
| `amount` | number |  |
| `batchPayment` | string |  |
| `canceledAt` | date |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `exchangeRate` | number |  |
| `id` | string |  |
| `installment` | number |  |
| `invoice` | string |  |
| `invoiceUuid` | string |  |
| `outstandingBalance` | number |  |
| `previousBalance` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /invoices/payments/:id` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-payment.md) for the provider-specific parameters and requirements.

