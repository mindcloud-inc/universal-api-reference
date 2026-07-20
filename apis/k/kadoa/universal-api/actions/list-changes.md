# Kadoa: List Changes



```
GET https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-changes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-changes?${params}`, {
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
      "changes": [
        {}
      ],
      "changesCount": 1,
      "pagination": {
        "limit": 1,
        "page": 1,
        "totalCount": 1,
        "totalPages": 1
      },
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changes` | array<object> |  |
| `changesCount` | number |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.totalCount` | number |  |
| `pagination.totalPages` | number |  |
| `timestamp` | date |  |

## Native endpoint

Through the native Kadoa API, this operation is `GET /v4/changes` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-changes.md) for the provider-specific parameters and requirements.

