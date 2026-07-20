# Bexio: List Invoices

Retrieves invoices from Bexio.

```
GET https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-invoices?${params}`, {
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
| `orderBy` | list<string> | no | Defines the order of the results. Multiple sort parameters can be combined with a comma separator. `_asc` and `_desc` can be appended to any parameter to sort ascending or descending. One of: `id`, `total`, `total_gross`, `total_net`, `updated_at`. |

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

Through the native Bexio API, this operation is `GET /2.0/kb_invoice` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

