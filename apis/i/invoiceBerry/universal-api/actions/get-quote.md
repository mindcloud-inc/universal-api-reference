# InvoiceBerry: Get Quote



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-quote?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-quote?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "client_firstname": "Ava",
      "client_id": "string",
      "client_lastname": "Chen",
      "client_name": "Ava Chen",
      "currency": "string",
      "date_of_issue": "2026-05-07T12:00:00.000Z",
      "discount": "string",
      "expire_term_days": "string",
      "id": "string",
      "items": [
        {}
      ],
      "language": "string",
      "notes": "string",
      "po_number": "string",
      "quote_number": "string",
      "quote_status": "string",
      "terms": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_firstname` | string |  |
| `client_id` | string |  |
| `client_lastname` | string |  |
| `client_name` | string |  |
| `currency` | string |  |
| `date_of_issue` | date |  |
| `discount` | string |  |
| `expire_term_days` | string |  |
| `id` | string |  |
| `items` | array<object> |  |
| `language` | string |  |
| `notes` | string |  |
| `po_number` | string |  |
| `quote_number` | string |  |
| `quote_status` | string |  |
| `terms` | string |  |
| `total` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quote.md) for the provider-specific parameters and requirements.

