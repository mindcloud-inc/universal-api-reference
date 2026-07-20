# Quentn: List Users



```
GET https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-users?${params}`, {
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
      "limit": 1,
      "numberRanges": 1,
      "numberUsers": "string",
      "range": 1,
      "sort": "string",
      "users": [
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
| `limit` | number | The page size returned by Quentn. |
| `numberRanges` | number | The total number of available ranges returned by Quentn. |
| `numberUsers` | string | The total number of Quentn users returned by the request. |
| `range` | number | The current pagination offset returned by Quentn. |
| `sort` | string | The sort direction returned by Quentn. |
| `users` | array<object> | The list of Quentn users. |

## Native endpoint

Through the native Quentn API, this operation is `GET /users` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

