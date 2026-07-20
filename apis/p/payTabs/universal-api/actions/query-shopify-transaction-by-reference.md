# PayTabs: Query Shopify Transaction by Reference



```
GET https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-shopify-transaction-by-reference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-shopify-transaction-by-reference?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-shopify-transaction-by-reference?${params}`, {
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
      "cartId": "string",
      "message": "string",
      "tranRef": "string",
      "transactions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartId` | string |  |
| `message` | string |  |
| `tranRef` | string |  |
| `transactions` | array<object> |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/query` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-shopify-transaction-by-reference.md) for the provider-specific parameters and requirements.

