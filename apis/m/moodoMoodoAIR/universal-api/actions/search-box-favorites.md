# Moodo & Moodo AIR: Search Box Favorites

Finds favorites for a Moodo box by title.

```
GET https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/search-box-favorites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/search-box-favorites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/search-box-favorites?${params}`, {
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
      "favorites": [
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
| `favorites` | array<object> |  |

## Native endpoint

Through the native Moodo & Moodo AIR API, this operation is `GET /favorites/:filter_my_favorites/:device_key/:search_favorite_title` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-box-favorites.md) for the provider-specific parameters and requirements.

