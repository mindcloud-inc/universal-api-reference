# Bexio: Get Invoice

Retrieves an invoice from Bexio.

```
GET https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | number | yes | The ID of the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiReference": "string",
      "bankAccountId": 1,
      "contactAddress": "string",
      "contactId": 1,
      "contactSubId": {},
      "currencyId": 1,
      "documentNr": "string",
      "esrId": 1,
      "footer": "string",
      "header": "string",
      "id": 1,
      "isValidFrom": "2026-05-07T12:00:00.000Z",
      "isValidTo": "2026-05-07T12:00:00.000Z",
      "kbItemStatusId": 1,
      "languageId": 1,
      "logopaperId": 1,
      "mwstIsNet": true,
      "mwstType": 1,
      "networkLink": "https://example.com",
      "paymentTypeId": 1,
      "positions": [
        {
          "accountId": 1,
          "amount": "string",
          "amountCompleted": "string",
          "amountOpen": "string",
          "amountReserved": "string",
          "discountInPercent": {},
          "id": 1,
          "internalPos": 1,
          "isOptional": true,
          "parentId": {},
          "pos": "string",
          "positionTotal": "string",
          "taxId": 1,
          "taxValue": "string",
          "text": "string",
          "type": "string",
          "unitId": {},
          "unitName": {},
          "unitPrice": "string"
        }
      ],
      "projectId": {},
      "qrInvoiceId": 1,
      "reference": "string",
      "showPositionTaxes": true,
      "taxs": [
        {
          "percentage": "string",
          "value": "string"
        }
      ],
      "templateSlug": "string",
      "title": "string",
      "total": "string",
      "totalCreditVouchers": "string",
      "totalGross": "string",
      "totalNet": "string",
      "totalReceivedPayments": "string",
      "totalRemainingPayments": "string",
      "totalRoundingDifference": 1,
      "totalTaxes": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "viewedByClientAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiReference` | string |  |
| `bankAccountId` | number |  |
| `contactAddress` | string |  |
| `contactId` | number |  |
| `contactSubId` | object |  |
| `currencyId` | number |  |
| `documentNr` | string |  |
| `esrId` | number |  |
| `footer` | string |  |
| `header` | string |  |
| `id` | number |  |
| `isValidFrom` | date |  |
| `isValidTo` | date |  |
| `kbItemStatusId` | number |  |
| `languageId` | number |  |
| `logopaperId` | number |  |
| `mwstIsNet` | boolean |  |
| `mwstType` | number |  |
| `networkLink` | string |  |
| `paymentTypeId` | number |  |
| `positions[].accountId` | number |  |
| `positions[].amount` | string |  |
| `positions[].amountCompleted` | string |  |
| `positions[].amountOpen` | string |  |
| `positions[].amountReserved` | string |  |
| `positions[].discountInPercent` | object |  |
| `positions[].id` | number |  |
| `positions[].internalPos` | number |  |
| `positions[].isOptional` | boolean |  |
| `positions[].parentId` | object |  |
| `positions[].pos` | string |  |
| `positions[].positionTotal` | string |  |
| `positions[].taxId` | number |  |
| `positions[].taxValue` | string |  |
| `positions[].text` | string |  |
| `positions[].type` | string |  |
| `positions[].unitId` | object |  |
| `positions[].unitName` | object |  |
| `positions[].unitPrice` | string |  |
| `projectId` | object |  |
| `qrInvoiceId` | number |  |
| `reference` | string |  |
| `showPositionTaxes` | boolean |  |
| `taxs[].percentage` | string |  |
| `taxs[].value` | string |  |
| `templateSlug` | string |  |
| `title` | string |  |
| `total` | string |  |
| `totalCreditVouchers` | string |  |
| `totalGross` | string |  |
| `totalNet` | string |  |
| `totalReceivedPayments` | string |  |
| `totalRemainingPayments` | string |  |
| `totalRoundingDifference` | number |  |
| `totalTaxes` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `viewedByClientAt` | date |  |

## Native endpoint

Through the native Bexio API, this operation is `GET /2.0/kb_invoice/:invoice_id` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

