# Zoho Books: Update Invoice



```
PUT https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": "string",
  "customerId": "string",
  "lineItems[]": [
    {}
  ],
  "lineItems[].itemId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": "string",
    "customerId": "string",
    "lineItems[]": [{}],
    "lineItems[].itemId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | string | yes | Unique identifier of the invoice to update. |
| `customerId` | string | yes | Unique identifier of the customer for whom the invoice is created. |
| `invoiceNumber` | string | no | Custom invoice number when auto-number generation is disabled. |
| `date` | date | no | Invoice date in yyyy-mm-dd format. |
| `dueDate` | date | no | Invoice due date in yyyy-mm-dd format. |
| `referenceNumber` | string | no | External reference number for the invoice. |
| `notes` | string | no | Notes printed on the invoice. |
| `terms` | string | no | Terms and conditions for the invoice. |
| `lineItems[]` | array<object> | yes | Line items to include on the invoice. |
| `lineItems[].itemId` | string | yes | Unique identifier of the item to bill. |
| `lineItems[].name` | string | no | Display name for the line item. |
| `lineItems[].description` | string | no | Description for the line item. |
| `lineItems[].rate` | number | no | Unit rate for the line item. |
| `lineItems[].quantity` | number | no | Quantity for the line item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreAutoNumberGeneration` | boolean | no | Require a custom invoice number instead of auto-generation. |
| `lineItems[].lineItemId` | string | no | Unique identifier of an existing invoice line item. |

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

Through the native Zoho Books API, this operation is `PUT /invoices/:invoice_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

