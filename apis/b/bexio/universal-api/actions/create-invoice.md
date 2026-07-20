# Bexio: Create Invoice

Creates an invoice in Bexio.

```
POST https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentNr` | string | no | Can not be used if automatic numbering is activated in frontend settings. Required if automatic numbering is deactivated. |
| `positions[].amount` | string | no | Invoice position amount. |
| `positions[].text` | string | no | Invoice position text. |
| `positions[].type` | string | no | Invoice position type. |
| `positions[].unitPrice` | string | no | Invoice position unit price. |
| `title` | string | no | The invoice title. |
| `contactId` | number | no | References a contact object. |
| `contactSubId` | number | no | References a contact object. |
| `userId` | number | no | References a user object. |
| `prProjectId` | number | no | References a project object. |
| `logopaperId` | number | no | The logopaper ID. |
| `languageId` | number | no | References a language object. |
| `bankAccountId` | number | no | References a bank account object. |
| `currencyId` | number | no | References a currency object. |
| `paymentTypeId` | number | no | References a payment type object. |
| `header` | string | no | The invoice header text. |
| `footer` | string | no | The invoice footer text. |
| `mwstType` | number | no | Tax calculation mode for the invoice. |
| `mwstIsNet` | boolean | no | Whether taxes should be added to the total when mwst_type is 0. |
| `showPositionTaxes` | boolean | no | Whether to show taxes for each position. |
| `isValidFrom` | date | no | The date from which the invoice is valid. |
| `isValidTo` | date | no | The date until which the invoice is valid. |
| `contactAddressManual` | string | no | Use a custom invoice address instead of the contact invoice address. |
| `reference` | string | no | The invoice reference. |
| `apiReference` | string | no | Reference value for other systems. |
| `templateSlug` | string | no | References a document template slug. |
| `positions[]` | array<object> | no | Invoice positions payload. |

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
      "projectId": {},
      "qrInvoiceId": 1,
      "reference": "string",
      "showPositionTaxes": true,
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
| `projectId` | object |  |
| `qrInvoiceId` | number |  |
| `reference` | string |  |
| `showPositionTaxes` | boolean |  |
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

Through the native Bexio API, this operation is `POST /2.0/kb_invoice` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

