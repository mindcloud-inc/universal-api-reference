# YouTube: List Video Categories

Retrieves available video categories from YouTube.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-video-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-video-categories?connectionId=$CONNECTION_ID&part=snippet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "part": "snippet"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-video-categories?${params}`, {
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
| `part` | string | yes | Comma-separated videoCategory resource parts to include. Default: `snippet`. |
| `regionCode` | string | no | ISO 3166-1 alpha-2 region code. Default: `US`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Comma-separated list of video category IDs. |
| `hl` | string | no | UI language code for localized metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `snippet` | object |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/videoCategories` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-video-categories.md) for the provider-specific parameters and requirements.

