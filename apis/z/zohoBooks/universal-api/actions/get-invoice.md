# Zoho Books: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | string | yes | Unique identifier of the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "billingAddress": {},
      "contact": {},
      "contactPersons": [
        "string"
      ],
      "contactPersonsAssociated": [
        {}
      ],
      "createdDate": "2026-05-07T12:00:00.000Z",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "currencySymbol": "string",
      "currentSubStatus": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "invoiceId": "string",
      "invoiceNumber": "string",
      "invoiceUrl": "https://example.com",
      "isEmailed": true,
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "lineItems": [
        {}
      ],
      "notes": "string",
      "paymentTerms": 1,
      "paymentTermsLabel": "string",
      "referenceNumber": "string",
      "salesChannel": "string",
      "shippingAddress": {},
      "status": "string",
      "subTotal": 1,
      "tags": [
        {}
      ],
      "taxTotal": 1,
      "templateId": "string",
      "templateName": "Ava Chen",
      "templateType": "string",
      "terms": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `billingAddress` | object |  |
| `contact` | object |  |
| `contactPersons` | array<string> |  |
| `contactPersonsAssociated` | array<object> |  |
| `createdDate` | date |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `currencySymbol` | string |  |
| `currentSubStatus` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `date` | date |  |
| `dueDate` | date |  |
| `email` | string |  |
| `invoiceId` | string |  |
| `invoiceNumber` | string |  |
| `invoiceUrl` | string |  |
| `isEmailed` | boolean |  |
| `lastModifiedTime` | date |  |
| `lineItems` | array<object> |  |
| `notes` | string |  |
| `paymentTerms` | number |  |
| `paymentTermsLabel` | string |  |
| `referenceNumber` | string |  |
| `salesChannel` | string |  |
| `shippingAddress` | object |  |
| `status` | string |  |
| `subTotal` | number |  |
| `tags` | array<object> |  |
| `taxTotal` | number |  |
| `templateId` | string |  |
| `templateName` | string |  |
| `templateType` | string |  |
| `terms` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /invoices/:invoice_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

