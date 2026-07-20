# Jooto: List Public Favorite Boards

Retrieves favorite boards from Jooto's public API.

```
GET https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-favorite-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jooto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-favorite-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-public-favorite-boards?${params}`, {
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
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Unique identifier for the board. |

## Native endpoint

Through the native Jooto API, this operation is `GET /api/public/v1/boards/favorites` (base URL `https://app.jooto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-favorite-boards.md) for the provider-specific parameters and requirements.

