# InvoiceBerry: List Recurring Invoices



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-recurring-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-recurring-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-recurring-invoices?${params}`, {
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
| `apiKey` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_send": "string",
      "client_name": "Ava Chen",
      "currency": "string",
      "end_date": "string",
      "frequency": "string",
      "id": "string",
      "last_invoice_date": "2026-05-07T12:00:00.000Z",
      "profile_number": "string",
      "start_date": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_send` | string |  |
| `client_name` | string |  |
| `currency` | string |  |
| `end_date` | string |  |
| `frequency` | string |  |
| `id` | string |  |
| `last_invoice_date` | date |  |
| `profile_number` | string |  |
| `start_date` | string |  |
| `total` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recurring-invoices.md) for the provider-specific parameters and requirements.

