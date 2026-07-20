# PayTabs: Query Transaction by Reference



```
GET https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-transaction-by-reference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-transaction-by-reference?connectionId=$CONNECTION_ID&tran_ref=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tran_ref": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-transaction-by-reference?${params}`, {
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
| `tran_ref` | string | yes | Unique PayTabs transaction reference to query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cartId": "string",
      "code": 1,
      "message": "string",
      "paymentResult": {},
      "profileId": 1,
      "trace": "string",
      "tranRef": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartId` | string |  |
| `code` | number |  |
| `message` | string |  |
| `paymentResult` | object |  |
| `profileId` | number |  |
| `trace` | string |  |
| `tranRef` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/query` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-transaction-by-reference.md) for the provider-specific parameters and requirements.

