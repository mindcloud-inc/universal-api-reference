# Kiwili: Get Invoice Payment Details

Retrieves details for an invoice payment in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-invoice-payment-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-invoice-payment-details?connectionId=$CONNECTION_ID&invoice_payment_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoice_payment_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-invoice-payment-details?${params}`, {
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
| `invoice_payment_id` | number | yes | The Kiwili invoice payment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Amount": 1,
      "Id": 1,
      "InvoiceId": 1,
      "Number": "string",
      "PaymentDate": "string",
      "TypeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Amount` | number |  |
| `Id` | number |  |
| `InvoiceId` | number |  |
| `Number` | string |  |
| `PaymentDate` | string |  |
| `TypeId` | number |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /invoicepayment/:invoice_payment_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-payment-details.md) for the provider-specific parameters and requirements.

