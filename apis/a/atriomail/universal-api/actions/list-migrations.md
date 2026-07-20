# Atriomail: List Migrations



```
GET https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-migrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atriomail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-migrations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-migrations?${params}`, {
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
      "jobs": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobs` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Atriomail API, this operation is `GET /migrations` (base URL `https://system.atriomail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-migrations.md) for the provider-specific parameters and requirements.

