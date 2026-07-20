# PayTabs: Download Invoice PDF



```
GET https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/download-invoice-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/download-invoice-pdf?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/download-invoice-pdf?${params}`, {
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
      "code": 1,
      "invoiceId": "string",
      "message": "string",
      "pdfUrl": "https://example.com",
      "trace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `invoiceId` | string |  |
| `message` | string |  |
| `pdfUrl` | string |  |
| `trace` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `GET /payment/invoice/{invoice_id}/download/pdf` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-invoice-pdf.md) for the provider-specific parameters and requirements.

