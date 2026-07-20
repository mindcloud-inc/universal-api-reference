# Freepik: Get Music

Retrieves detailed music information from Freepik.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-music
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-music?connectionId=$CONNECTION_ID&musicId=140" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "musicId": "140"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-music?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `musicId` | number | yes | Freepik music track identifier. Default: `140`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "artist": {},
      "cover_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "downloads": 1,
      "file_url": "https://example.com",
      "genres": [
        {}
      ],
      "id": 1,
      "moods": [
        {}
      ],
      "popularity": 1,
      "preview_url": "https://example.com",
      "seconds": 1,
      "time": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `artist` | object | Artist details. |
| `cover_url` | string | Cover image URL. |
| `created_at` | date | Creation timestamp. |
| `downloads` | number | Download count. |
| `file_url` | string | Track file URL. |
| `genres` | array<object> | Genres. |
| `id` | number | Music track ID. |
| `moods` | array<object> | Moods. |
| `popularity` | number | Popularity score. |
| `preview_url` | string | Preview audio URL. |
| `seconds` | number | Duration in seconds. |
| `time` | string | Duration label. |
| `title` | string | Track title. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/music/{{music-id}}` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-music.md) for the provider-specific parameters and requirements.

