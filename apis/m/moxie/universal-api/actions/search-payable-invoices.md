# Moxie: Search Payable Invoices

Finds payable invoices in Moxie.

```
GET https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-payable-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-payable-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-payable-invoices?${params}`, {
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
| `query` | string | no | Optional client name filter if you only want invoices for a specific client. Example: `Moxie, Inc.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "amountDue": 1,
      "clientId": "string",
      "clientInfo": {},
      "convenienceFee": 1,
      "creditApplied": 1,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateDue": "2026-05-07T12:00:00.000Z",
      "dateDueCalculated": "2026-05-07T12:00:00.000Z",
      "datePaid": "2026-05-07T12:00:00.000Z",
      "dateSent": "2026-05-07T12:00:00.000Z",
      "discountAmount": 1,
      "id": "string",
      "integrationKeys": {},
      "invoiceNumber": 1,
      "invoiceNumberFormatted": "string",
      "invoiceType": "string",
      "lateFee": 1,
      "localAmountDue": 1,
      "localPaymentTotal": 1,
      "localTotal": 1,
      "payments": [
        {}
      ],
      "paymentTotal": 1,
      "status": "string",
      "subTotal": 1,
      "tax": 1,
      "total": 1,
      "viewOnlineUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `amountDue` | number |  |
| `clientId` | string |  |
| `clientInfo` | object |  |
| `convenienceFee` | number |  |
| `creditApplied` | number |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `dateDue` | date |  |
| `dateDueCalculated` | date |  |
| `datePaid` | date |  |
| `dateSent` | date |  |
| `discountAmount` | number |  |
| `id` | string |  |
| `integrationKeys` | object |  |
| `invoiceNumber` | number |  |
| `invoiceNumberFormatted` | string |  |
| `invoiceType` | string |  |
| `lateFee` | number |  |
| `localAmountDue` | number |  |
| `localPaymentTotal` | number |  |
| `localTotal` | number |  |
| `payments` | array<object> |  |
| `paymentTotal` | number |  |
| `status` | string |  |
| `subTotal` | number |  |
| `tax` | number |  |
| `total` | number |  |
| `viewOnlineUrl` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `GET /action/payableInvoices/search` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-payable-invoices.md) for the provider-specific parameters and requirements.

