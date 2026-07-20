# Fliz: List musics

Retrieves available background music tracks from Fliz.

```
GET https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-musics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-musics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-musics?${params}`, {
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
      "name": "Ava Chen",
      "theme": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Music track ID. |
| `name` | string | Music track name. |
| `theme` | string | Music theme category. |
| `url` | string | Music file URL. |

## Native endpoint

Through the native Fliz API, this operation is `GET /api/rest/musics` (base URL `https://app.fliz.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-musics.md) for the provider-specific parameters and requirements.

