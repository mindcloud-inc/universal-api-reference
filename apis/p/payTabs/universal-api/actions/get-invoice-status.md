# PayTabs: Get Invoice Status



```
GET https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-invoice-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-invoice-status?connectionId=$CONNECTION_ID&invoice_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoice_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-invoice-status?${params}`, {
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
| `invoice_id` | string | yes | Invoice identifier to inspect. |

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

Through the native PayTabs API, this operation is `POST /payment/invoice/status` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-status.md) for the provider-specific parameters and requirements.

