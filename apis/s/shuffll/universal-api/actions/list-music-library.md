# Shuffll: List Music Library

Retrieves music library items from Shuffll.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-music-library
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-music-library?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-music-library?${params}`, {
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
      "id": "string",
      "image": "string",
      "name": "Ava Chen",
      "relativePath": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Track id. |
| `image` | string | Track preview image path. |
| `name` | string | Track name. |
| `relativePath` | string | Track audio path. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/config/music-library` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-music-library.md) for the provider-specific parameters and requirements.

