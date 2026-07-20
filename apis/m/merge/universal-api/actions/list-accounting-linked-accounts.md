# Merge: List Accounting Linked Accounts



```
GET https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-accounting-linked-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-accounting-linked-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-accounting-linked-accounts?${params}`, {
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
      "next": "string",
      "previous": "string",
      "results": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next` | string |  |
| `previous` | string |  |
| `results` | array |  |

## Native endpoint

Through the native Merge API, this operation is `GET /api/accounting/v1/linked-accounts` (base URL `https://api.merge.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounting-linked-accounts.md) for the provider-specific parameters and requirements.

