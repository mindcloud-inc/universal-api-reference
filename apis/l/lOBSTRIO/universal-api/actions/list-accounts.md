# LOBSTR.IO: List Accounts

Retrieves accounts from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/list-accounts?${params}`, {
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
      "data": [
        {}
      ],
      "limit": 1,
      "page": 1,
      "resultFrom": 1,
      "resultTo": 1,
      "totalPages": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `limit` | number |  |
| `page` | number |  |
| `resultFrom` | number |  |
| `resultTo` | number |  |
| `totalPages` | number |  |
| `totalResults` | number |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/accounts` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

