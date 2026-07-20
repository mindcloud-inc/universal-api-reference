# Syntage: Get Invoice

Retrieves an invoice from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-invoice?${params}`, {
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
| `id` | string | yes | The invoice identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@id": "string",
      "@type": "string",
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "cancellationProcessStatus": "string",
      "cancellationStatus": "string",
      "certifiedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "string",
      "creditedAmount": 1,
      "currency": "string",
      "discount": 1,
      "dueAmount": 1,
      "exchangeRate": 1,
      "fullyPaidAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "internalIdentifier": "string",
      "isIssuer": true,
      "isReceiver": true,
      "issuedAt": "2026-05-07T12:00:00.000Z",
      "issuer": {},
      "lastPaymentDate": "2026-05-07T12:00:00.000Z",
      "pac": "string",
      "paidAmount": 1,
      "paymentMethod": "string",
      "paymentTerms": "string",
      "paymentTermsRaw": "string",
      "paymentType": "string",
      "pdf": true,
      "placeOfIssue": "string",
      "receiver": {},
      "reference": "string",
      "relations": [
        {}
      ],
      "status": "string",
      "subtotal": 1,
      "subtotalCreditedAmount": 1,
      "tax": 1,
      "total": 1,
      "type": "string",
      "updatedAt": "string",
      "usage": "string",
      "uuid": "string",
      "version": 1,
      "xml": true
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
| `canceledAt` | date |  |
| `cancellationProcessStatus` | string |  |
| `cancellationStatus` | string |  |
| `certifiedAt` | date |  |
| `createdAt` | string |  |
| `creditedAmount` | number |  |
| `currency` | string |  |
| `discount` | number |  |
| `dueAmount` | number |  |
| `exchangeRate` | number |  |
| `fullyPaidAt` | date |  |
| `id` | string |  |
| `internalIdentifier` | string |  |
| `isIssuer` | boolean |  |
| `isReceiver` | boolean |  |
| `issuedAt` | date |  |
| `issuer` | object |  |
| `lastPaymentDate` | date |  |
| `pac` | string |  |
| `paidAmount` | number |  |
| `paymentMethod` | string |  |
| `paymentTerms` | string |  |
| `paymentTermsRaw` | string |  |
| `paymentType` | string |  |
| `pdf` | boolean |  |
| `placeOfIssue` | string |  |
| `receiver` | object |  |
| `reference` | string |  |
| `relations` | array<object> |  |
| `status` | string |  |
| `subtotal` | number |  |
| `subtotalCreditedAmount` | number |  |
| `tax` | number |  |
| `total` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `usage` | string |  |
| `uuid` | string |  |
| `version` | number |  |
| `xml` | boolean |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /invoices/:id` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

