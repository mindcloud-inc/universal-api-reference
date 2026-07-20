# Refrens: Generate Invoice IRN



```
POST https://connect.mindcloud.co/v1/universal/refrens/latest/actions/generate-invoice-irn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/generate-invoice-irn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/generate-invoice-irn', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoice` | string | yes |  |
| `includePaymentDetails` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AckDt": "string",
      "AckNo": "string",
      "invoiceId": "string",
      "invoiceNumber": "string",
      "Irn": "string",
      "qr": "string",
      "SignedInvoice": "string",
      "SignedQRCode": "string",
      "Status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AckDt` | string |  |
| `AckNo` | string |  |
| `invoiceId` | string |  |
| `invoiceNumber` | string |  |
| `Irn` | string |  |
| `qr` | string |  |
| `SignedInvoice` | string |  |
| `SignedQRCode` | string |  |
| `Status` | string |  |

## Native endpoint

Through the native Refrens API, this operation is `POST /businesses/:urlKey/invoices/:invoice/irn` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-invoice-irn.md) for the provider-specific parameters and requirements.

