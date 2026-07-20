# InvoiceBerry: List Credit Notes



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-credit-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-credit-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-credit-notes?${params}`, {
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
      "client_name": "Ava Chen",
      "credit_note_number": "string",
      "currency": "string",
      "doi": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_name` | string |  |
| `credit_note_number` | string |  |
| `currency` | string |  |
| `doi` | date |  |
| `id` | string |  |
| `status` | string |  |
| `total` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-credit-notes.md) for the provider-specific parameters and requirements.

