# InvoiceBerry: Get Client



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-client?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-client?${params}`, {
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
      "city": "string",
      "client_name": "Ava Chen",
      "contacts": [
        {}
      ],
      "country": "string",
      "country_iso": "string",
      "currency": "string",
      "fax": "string",
      "id": "string",
      "language": "string",
      "notes": "string",
      "phone": "string",
      "state": "string",
      "street1": "string",
      "street2": "string",
      "tax_name": "Ava Chen",
      "tax_number": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `client_name` | string |  |
| `contacts` | array<object> |  |
| `country` | string |  |
| `country_iso` | string |  |
| `currency` | string |  |
| `fax` | string |  |
| `id` | string |  |
| `language` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `street1` | string |  |
| `street2` | string |  |
| `tax_name` | string |  |
| `tax_number` | string |  |
| `zip_code` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

