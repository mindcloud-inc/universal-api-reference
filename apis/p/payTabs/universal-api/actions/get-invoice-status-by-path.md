# PayTabs: Get Invoice Status by Path



```
GET https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-invoice-status-by-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-invoice-status-by-path?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-invoice-status-by-path?${params}`, {
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
      "invoiceStatus": "string",
      "invoiceUrl": "https://example.com",
      "message": "string",
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
| `invoiceStatus` | string |  |
| `invoiceUrl` | string |  |
| `message` | string |  |
| `trace` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `GET /payment/invoice/{invoice_id}/status` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-status-by-path.md) for the provider-specific parameters and requirements.

