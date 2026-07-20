# QuickFile: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | number | yes | The QuickFile InvoiceID to retrieve. |

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

Through the native QuickFile API, this operation is `POST /invoice/get` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

