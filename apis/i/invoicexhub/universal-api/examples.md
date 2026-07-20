# Invoice.xhub Universal API Examples

These examples use the MindCloud API key and Invoice.xhub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Supported Formats



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-all-supported-formats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-all-supported-formats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "countries": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get All Supported Formats action reference](actions/get-all-supported-formats.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invoicexhub/latest/actions/get-all-supported-formats).

## Generate Austria ebInterface Invoice



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/generate-austria-eb-interface-invoice" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/generate-austria-eb-interface-invoice', {
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

Example response:

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

See the full [Generate Austria ebInterface Invoice action reference](actions/generate-austria-eb-interface-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invoicexhub/latest/actions/generate-austria-eb-interface-invoice).
