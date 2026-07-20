# QuickFile: Search Invoices



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-invoices?${params}`, {
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
| `limit` | number | no | How many invoices to return, up to 200. Default: `2`. |
| `offset` | number | no | Page offset starting at 0. Default: `0`. |
| `sortBy` | string | no | Field used to order invoice search results. Default: `IssueDate`. |
| `sortDirection` | string | no | Order direction for invoice search results. Default: `DESC`. |
| `clientName` | string | no | Whole or part of the client company name. |
| `issueDateFrom` | date | no | Issued date range start. |
| `issueDateTo` | date | no | Issued date range end. |
| `amountFrom` | number | no | Minimum invoice amount. |
| `amountTo` | number | no | Maximum invoice amount. |
| `status` | string | no | Invoice status to search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientName": "Ava Chen",
      "currency": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "invoiceId": 1,
      "invoiceNumber": "string",
      "issueDate": "2026-05-07T12:00:00.000Z",
      "netAmount": 1,
      "status": "string",
      "totalAmount": 1,
      "vatAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientName` | string | Name of the invoice customer. |
| `currency` | string | Invoice currency. |
| `dueDate` | date | Invoice due date. |
| `invoiceId` | number | QuickFile invoice identifier. |
| `invoiceNumber` | string | Provider invoice number. |
| `issueDate` | date | Invoice issue date. |
| `netAmount` | number | Invoice net total. |
| `status` | string | QuickFile invoice status. |
| `totalAmount` | number | Invoice gross total. |
| `vatAmount` | number | Invoice tax amount. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /invoice/search` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-invoices.md) for the provider-specific parameters and requirements.

