# CoachAccountable: Create Invoice

Creates an invoice in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateOf": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateOf": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | no | The ID of the Client for whom this invoice is (if not for a Company). |
| `companyId` | number | no | The ID of the Company for whom this invoice is (if not for a Client). |
| `dateOf` | date | yes |  |
| `dateDue` | date | no | If omitted, the due date will be calculated based on the dateOf and your setting of how many days out invoices are due by default. |
| `number` | string | no | If not supplied, a logical next invoice number will be assigned. Letters are allowed, e.g. "A1002". |
| `taxRate` | number | no | A percentage-based rate of tax to be applied, e.g. 7.5 means apply a 7.5% tax. |
| `onDuplicateNumber` | list | no | What to do if an Invoice with the supplied number already exists. One of: `A`, `E`, `S`. Default: `S`. |
| `currency` | string | no | The ISO 4217 3-letter code of the currency. If not supplied, or not among the chosen accepted currencies, the chosen primary currency will be assumed. |
| `lineItemSet` | string | no | A newline-separated list of items. An item is comprised of the item label followed by a double colon followed by the price. For example: "One month of coaching::400" |
| `collectPaymentIfPossible` | boolean | no | If set to "true", will try to collect full payment for the invoice immediately (using a client's card on file). To determine if the charge was successful, use Invoice.get. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "InvoiceID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `InvoiceID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

