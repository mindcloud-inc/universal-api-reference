# Dripcel: Search Transactions

Finds buyer transactions in Dripcel Exchange.

```
GET https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/search-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/search-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/search-transactions?${params}`, {
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
      "ok": true,
      "pagination": {
        "hasNext": true,
        "limit": 1,
        "nextCursor": {}
      },
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `pagination.hasNext` | boolean |  |
| `pagination.limit` | number |  |
| `pagination.nextCursor` | object |  |
| `requestId` | string |  |

## Native endpoint

Through the native Dripcel API, this operation is `POST /exchange/buyer/transaction/search` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-transactions.md) for the provider-specific parameters and requirements.

