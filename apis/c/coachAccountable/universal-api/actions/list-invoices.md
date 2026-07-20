# CoachAccountable: List Invoices

Retrieves invoices from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-invoices?${params}`, {
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
| `clientId` | number | no | Filter invoices by client. If this and CompanyID are omitted, invoices for all invoicees are returned. |
| `companyId` | number | no | Filter invoices by Company. If this and ClientID are omitted, invoices for all invoicees are returned. |
| `dateFrom` | date | no | Set to restrict Invoices returned to those at or after the provided value. |
| `dateTo` | date | no | Set to restrict Invoices returned to those at or before the provided value. |
| `sortField` | list | no | One of: `dateAdded`, `dateDue`, `dateOf`. Default: `dateAdded`. |
| `sortDirection` | list | no | One of: `A`, `D`. Default: `D`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountPaid": 1,
      "ClientID": 1,
      "CompanyID": 1,
      "companyName": "Ava Chen",
      "currency": "string",
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "dateDue": "2026-05-07T12:00:00.000Z",
      "dateOf": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "ID": 1,
      "invoiceNumber": "string",
      "lastName": "Chen",
      "lineItemSet": [
        {
          "amount": 1,
          "item": "string"
        }
      ],
      "paymentSet": [
        {
          "amount": 1,
          "checkNumber": "string",
          "datePaid": "2026-05-07T12:00:00.000Z",
          "method": "string"
        }
      ],
      "taxRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `amountPaid` | number |  |
| `ClientID` | number |  |
| `CompanyID` | number |  |
| `companyName` | string |  |
| `currency` | string |  |
| `dateAdded` | date |  |
| `dateDue` | date |  |
| `dateOf` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `ID` | number |  |
| `invoiceNumber` | string |  |
| `lastName` | string |  |
| `lineItemSet` | array<object> |  |
| `lineItemSet[].amount` | number |  |
| `lineItemSet[].item` | string |  |
| `paymentSet` | array<object> |  |
| `paymentSet[].amount` | number |  |
| `paymentSet[].checkNumber` | string |  |
| `paymentSet[].datePaid` | date |  |
| `paymentSet[].method` | string |  |
| `taxRate` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

