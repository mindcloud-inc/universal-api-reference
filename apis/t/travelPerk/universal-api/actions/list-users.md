# TravelPerk: List Users

Retrieves user information from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-users?${params}`, {
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
      "offset": 1,
      "total": 1,
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
| `limit` | number |  |
| `offset` | number |  |
| `total` | number |  |
| `users` | array<object> |  |

## Native endpoint

Through the native TravelPerk API, this operation is `GET /users` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

