# Bexio: Create Quote

Creates a quote in Bexio.

```
POST https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-quote', {
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
| `contactId` | number | no | Contact ID. Example: `1`. |
| `userId` | number | no | User ID. Example: `1`. |
| `documentNr` | string | no | Quote document number. Example: `Q-1001`. |
| `title` | string | no | Quote title. Example: `Consulting Quote`. |
| `positions[]` | array<object> | no | Quote positions array. |
| `languageId` | number | no | Language ID. Example: `1`. |
| `currencyId` | number | no | Currency ID. Example: `1`. |
| `paymentTypeId` | number | no | Payment type ID. Example: `1`. |
| `mwstType` | list<number> | no | Tax type. One of: `0`, `1`, `2`. |
| `isValidFrom` | date | no | Valid from date. Example: `2026-03-12`. |
| `isValidUntil` | date | no | Valid until date. Example: `2026-04-11`. |
| `header` | string | no | Header text. Example: `Thank you for your request`. |
| `footer` | string | no | Footer text. Example: `We look forward to working with you`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactSubId` | number | no | Contact sub ID. Example: `1`. |
| `prProjectId` | number | no | Project ID. Example: `1`. |
| `logopaperId` | number | no | Logo paper ID. Example: `1`. |
| `bankAccountId` | number | no | Bank account ID. Example: `1`. |
| `mwstIsNet` | boolean | no | Whether taxes are added to the total. |
| `showPositionTaxes` | boolean | no | Whether to show position taxes. |
| `contactAddressManual` | string | no | Manual contact address. Example: `Acme AG\nMain Street 1\n8000 Zurich`. |
| `deliveryAddressType` | list<number> | no | Delivery address type. One of: `0`, `1`. |
| `deliveryAddressManual` | string | no | Manual delivery address. Example: `Warehouse\nDock 2\n8000 Zurich`. |
| `kbTermsOfPaymentTemplateId` | number | no | Terms of payment template ID. Example: `1`. |
| `templateSlug` | string | no | Document template slug. Example: `default`. |
| `apiReference` | string | no | API-only external reference. Example: `external-quote-123`. |
| `viewedByClientAt` | string | no | Viewed-by-client timestamp. Example: `2026-03-12T10:00:00Z`. |

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
      "deliveryAddress": "string",
      "deliveryAddressType": 1,
      "documentNr": "string",
      "footer": "string",
      "header": "string",
      "id": 1,
      "isValidFrom": "2026-05-07T12:00:00.000Z",
      "isValidUntil": "2026-05-07T12:00:00.000Z",
      "kbItemStatusId": 1,
      "kbTermsOfPaymentTemplateId": {},
      "languageId": 1,
      "logopaperId": 1,
      "mwstIsNet": true,
      "mwstType": 1,
      "networkLink": "https://example.com",
      "paymentTypeId": 1,
      "projectId": {},
      "showPositionTaxes": true,
      "showTotal": true,
      "templateSlug": "string",
      "title": "string",
      "total": "string",
      "totalGross": "string",
      "totalNet": "string",
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
| `deliveryAddress` | string |  |
| `deliveryAddressType` | number |  |
| `documentNr` | string |  |
| `footer` | string |  |
| `header` | string |  |
| `id` | number |  |
| `isValidFrom` | date |  |
| `isValidUntil` | date |  |
| `kbItemStatusId` | number |  |
| `kbTermsOfPaymentTemplateId` | object |  |
| `languageId` | number |  |
| `logopaperId` | number |  |
| `mwstIsNet` | boolean |  |
| `mwstType` | number |  |
| `networkLink` | string |  |
| `paymentTypeId` | number |  |
| `projectId` | object |  |
| `showPositionTaxes` | boolean |  |
| `showTotal` | boolean |  |
| `templateSlug` | string |  |
| `title` | string |  |
| `total` | string |  |
| `totalGross` | string |  |
| `totalNet` | string |  |
| `totalRoundingDifference` | number |  |
| `totalTaxes` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `viewedByClientAt` | date |  |

## Native endpoint

Through the native Bexio API, this operation is `POST /2.0/kb_offer` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

