# CoachAccountable: List Invoice Payments

Retrieves invoice payments from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-invoice-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-invoice-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-invoice-payments?${params}`, {
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
| `dateFrom` | date | no | Set to restrict Invoice Payments returned to those at or after the provided value. |
| `dateTo` | date | no | Set to restrict Invoice Payments returned to those at or before the provided value. |
| `sortField` | list | no | One of: `datePaid`, `invoiceNumber`. Default: `datePaid`. |
| `sortDirection` | list | no | One of: `A`, `D`. Default: `D`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "checkNumber": "string",
      "currency": "string",
      "datePaid": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "InvoiceID": 1,
      "invoiceNumber": "string",
      "method": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `checkNumber` | string |  |
| `currency` | string |  |
| `datePaid` | date |  |
| `ID` | number |  |
| `InvoiceID` | number |  |
| `invoiceNumber` | string |  |
| `method` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoice-payments.md) for the provider-specific parameters and requirements.

