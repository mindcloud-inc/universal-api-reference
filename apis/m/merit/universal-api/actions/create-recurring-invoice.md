# Merit: Create Recurring Invoice



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-recurring-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-recurring-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": {},
  "startDate": "20260422",
  "nextDate": "20260422",
  "cycle": "1",
  "period": "2",
  "invoiceRow[]": [
    {}
  ],
  "taxAmount[]": [
    {}
  ],
  "totalAmount": 1,
  "totalSum": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-recurring-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": {},
    "startDate": "20260422",
    "nextDate": "20260422",
    "cycle": "1",
    "period": "2",
    "invoiceRow[]": [{}],
    "taxAmount[]": [{}],
    "totalAmount": 1,
    "totalSum": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | object | yes | Customer object. |
| `startDate` | string | yes | Recurring invoice start date in YYYYmmDD format. Example: `20260422`. |
| `nextDate` | string | yes | Next invoice date in YYYYmmDD format. Example: `20260422`. |
| `cycle` | number | yes | 1 month, 2 quarter, 3 year, 4 week. Example: `1`. |
| `period` | number | yes | Invoice period mode. Example: `2`. |
| `invoiceRow[]` | array<object> | yes | Array of invoice row objects. |
| `taxAmount[]` | array<object> | yes | Array of VAT amount objects. |
| `totalAmount` | number | yes | Total amount without VAT. |
| `totalSum` | number | yes | Total amount including VAT. |
| `currencyCode` | string | no | Invoice currency code. Example: `EUR`. |
| `code` | string | no | Recurring invoice code. |
| `invoiceNo` | string | no | Invoice number. |
| `hComment` | string | no | Header comment. |
| `fComment` | string | no | Footer comment. |
| `paymentDay` | number | no | Payment day. |
| `referenceNo` | string | no | Reference number. |
| `priceInclVat` | boolean | no | Whether prices include VAT. |
| `payer` | object | no | Optional payer object. |
| `endDate` | string | no | Recurring invoice end date in YYYYmmDD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merit API returns.

## Native endpoint

Through the native Merit API, this operation is `POST v2/sendperinvoice` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recurring-invoice.md) for the provider-specific parameters and requirements.

