# Pirsonal: List Video Links

Retrieves downloadable links for a Pirsonal video.

```
GET https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-video-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirsonal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-video-links?connectionId=$CONNECTION_ID&videoID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-video-links?${params}`, {
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
| `videoID` | string | yes | ID of the video whose links should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "profile": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Video link ID. |
| `profile` | string | Video link profile. |
| `url` | string | Video download URL. |

## Native endpoint

Through the native Pirsonal API, this operation is `POST /api` (base URL `https://app.pirsonal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-video-links.md) for the provider-specific parameters and requirements.

