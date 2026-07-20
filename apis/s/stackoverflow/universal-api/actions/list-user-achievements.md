# Stackoverflow: List User Achievements

Retrieves a user's achievements from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-achievements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-achievements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-achievements?${params}`, {
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
      "achievement_type": "string",
      "link": "https://example.com",
      "rank": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `achievement_type` | string |  |
| `link` | string |  |
| `rank` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /users/[:id]/achievements` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-achievements.md) for the provider-specific parameters and requirements.

