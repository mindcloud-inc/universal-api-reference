# VdoCipher: Get Video Chapters

Retrieves video chapters from VdoCipher.

```
GET https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video-chapters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video-chapters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video-chapters?${params}`, {
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
| `videoId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "startTime": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `startTime` | number |  |
| `title` | string |  |

## Native endpoint

Through the native VdoCipher API, this operation is `GET /videos/:videoId/chapters` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-chapters.md) for the provider-specific parameters and requirements.

