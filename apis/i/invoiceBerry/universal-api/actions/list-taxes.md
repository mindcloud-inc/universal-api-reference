# InvoiceBerry: List Taxes



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-taxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-taxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-taxes?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "number": "string",
      "percentage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | InvoiceBerry tax identifier. |
| `name` | string | Tax name. |
| `number` | string | Optional tax registration number. |
| `percentage` | string | Tax percentage value as returned by InvoiceBerry. |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-taxes.md) for the provider-specific parameters and requirements.

