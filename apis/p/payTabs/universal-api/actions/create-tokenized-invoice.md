# PayTabs: Create Tokenized Invoice



```
POST https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-tokenized-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-tokenized-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-tokenized-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
      "invoice": {},
      "invoiceId": "string",
      "invoiceStatus": "string",
      "invoiceUrl": "https://example.com",
      "message": "string",
      "tokenise": true,
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
| `invoice` | object |  |
| `invoiceId` | string |  |
| `invoiceStatus` | string |  |
| `invoiceUrl` | string |  |
| `message` | string |  |
| `tokenise` | boolean |  |
| `trace` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/new/invoice` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tokenized-invoice.md) for the provider-specific parameters and requirements.

