# InvoiceBerry: List Client Reports



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-client-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-client-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-client-reports?${params}`, {
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
      "average_sum": 1,
      "client_id": "string",
      "client_name": "Ava Chen",
      "currency": "string",
      "invoices": [
        {}
      ],
      "num_of_invoices": "string",
      "outstanding": 1,
      "received": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `average_sum` | number |  |
| `client_id` | string |  |
| `client_name` | string |  |
| `currency` | string |  |
| `invoices` | array<object> |  |
| `num_of_invoices` | string |  |
| `outstanding` | number |  |
| `received` | string |  |
| `total` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-reports.md) for the provider-specific parameters and requirements.

