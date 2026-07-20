# Invoice.xhub: Generate Bulgaria UBL Invoice



```
POST https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/generate-bulgaria-ubl-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice.xhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/generate-bulgaria-ubl-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": {
    "type": "invoice",
    "buyer": {
      "city": "Munich",
      "name": "BigCorp AG",
      "street": "Kundenweg 42",
      "postalCode": "80331",
      "countryCode": "DE"
    },
    "items": [
      {
        "unit": "EA",
        "taxRate": 19,
        "position": 1,
        "quantity": 1,
        "netAmount": 1500,
        "taxAmount": 285,
        "unitPrice": 1500,
        "description": "Software license",
        "grossAmount": 1785
      }
    ],
    "total": 1785,
    "seller": {
      "city": "Berlin",
      "name": "Acme GmbH",
      "email": "billing@acme.example",
      "vatId": "DE123456789",
      "street": "Musterstrasse 1",
      "postalCode": "10115",
      "countryCode": "DE"
    },
    "dueDate": "2025-02-15",
    "currency": "EUR",
    "subtotal": 1500,
    "issueDate": "2025-01-15",
    "taxSummary": [
      {
        "taxRate": 19,
        "netAmount": 1500,
        "taxAmount": 285,
        "taxableAmount": 1500
      }
    ],
    "paymentTerms": {
      "dueDate": "2025-02-15",
      "dueDays": 31
    },
    "invoiceNumber": "TEST-001"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/generate-bulgaria-ubl-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": {"type":"invoice","buyer":{"city":"Munich","name":"BigCorp AG","street":"Kundenweg 42","postalCode":"80331","countryCode":"DE"},"items":[{"unit":"EA","taxRate":19,"position":1,"quantity":1,"netAmount":1500,"taxAmount":285,"unitPrice":1500,"description":"Software license","grossAmount":1785}],"total":1785,"seller":{"city":"Berlin","name":"Acme GmbH","email":"billing@acme.example","vatId":"DE123456789","street":"Musterstrasse 1","postalCode":"10115","countryCode":"DE"},"dueDate":"2025-02-15","currency":"EUR","subtotal":1500,"issueDate":"2025-01-15","taxSummary":[{"taxRate":19,"netAmount":1500,"taxAmount":285,"taxableAmount":1500}],"paymentTerms":{"dueDate":"2025-02-15","dueDays":31},"invoiceNumber":"TEST-001"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoice` | object | yes | Invoice payload to generate. Default: `{"type":"invoice","buyer":{"city":"Munich","name":"BigCorp AG","street":"Kundenweg 42","postalCode":"80331","countryCode":"DE"},"items":[{"unit":"EA","taxRate":19,"position":1,"quantity":1,"netAmount":1500,"taxAmount":285,"unitPrice":1500,"description":"Software license","grossAmount":1785}],"total":1785,"seller":{"city":"Berlin","name":"Acme GmbH","email":"billing@acme.example","vatId":"DE123456789","street":"Musterstrasse 1","postalCode":"10115","countryCode":"DE"},"dueDate":"2025-02-15","currency":"EUR","subtotal":1500,"issueDate":"2025-01-15","taxSummary":[{"taxRate":19,"netAmount":1500,"taxAmount":285,"taxableAmount":1500}],"paymentTerms":{"dueDate":"2025-02-15","dueDays":31},"invoiceNumber":"TEST-001"}`. |
| `formatOptions` | object | no | Optional format-specific generation options. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "errors": [
        {}
      ],
      "filename": "Ava Chen",
      "format": "string",
      "hash": "string",
      "mimeType": "string",
      "success": true,
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `errors` | array<object> |  |
| `filename` | string |  |
| `format` | string |  |
| `hash` | string |  |
| `mimeType` | string |  |
| `success` | boolean |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Invoice.xhub API, this operation is `POST /api/v1/invoice/BG/UBL/generate` (base URL `https://service.invoice-api.xhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-bulgaria-ubl-invoice.md) for the provider-specific parameters and requirements.

